<pre>sudo apt-get install maven</pre>
1.7.2的es 要下载 <a href="https://github.com/medcl/elasticsearch-analysis-ik/tree/v1.4.1">1.4.1(点击下载)</a>的ik
<pre>
cd elasticsearch-analysis-ik
mvn compile
mvn package
拷贝elasticsearch-analysis-ik/target/releases/elasticsearch-analysis-ik-xxx-jar-with-dependencies.jar 到你的es文件夹: plugins/ik
</pre>
