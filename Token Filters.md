<h3词条过滤器(Token Filter)</h3> 
<pre>在分词后，得到的词条流(Token Stream)会按照顺序被传入到指定的词条过滤器中。
词条过滤器能够修改，增加或者删除词条
ascii_folding词条过滤器则会移除变音符号(Diacritics)，将类似于très的词条转换成tres。
ngram词条过滤器和edge_ngram词条过滤器会产生适用于部分匹配(Partial Matching)或者自动完成(Autocomplete)的词条。
</pre>
