<pre>sudo apt-get install maven</pre>
1.7.2的es 要下载 <a href="https://github.com/medcl/elasticsearch-analysis-ik/tree/v1.4.1">1.4.1(点击下载)</a>的ik
<pre>

cd elasticsearch-analysis-ik
mvn compile
mvn package
拷贝elasticsearch-analysis-ik/target/releases/elasticsearch-analysis-ik-xxx-jar-with-dependencies.jar 到ES_HOME/plugins/analysis-ik,如果没有这个文件夹就手动创建

配置elasticsearch-1.7.2/config/elasticsearch.yml,加入:
<code>
index:
  analysis:
    analyzer:
      ik:
          alias: [ik_analyzer]
          type: org.elasticsearch.index.analysis.IkAnalyzerProvider
      ik_max_word:
          type: ik
          use_smart: false
      ik_smart:
          type: ik
          use_smart: true
</code>
</pre>
重启:使用之前的管理插件<a target="_blank" href="https://github.com/elastic/elasticsearch-servicewrapper">elasticsearch-servicewrapper</a>重启
测试:
<pre>
curl -XPUT http://localhost:9200/index


</pre>

