博客地址：http://blog.csdn.net/b275518834/article/details/51509312


<p>
	最早使用android调用系统拍照然后遇到很多空指针等问题
</p>
<p>
	以及各种android 不同版本Intent取data有时候会空指针之类的api兼容问题
</p>
<p>
	像使用红米note在开了很多应用后，再启动拍照系统，会发生拍照崩溃图片丢失等问题<br />
	
</p>
<p>
	用微信控件有时拍照有极小概率拍照无效等等奇怪的问题
</p>
<p>
	其原因是因为Activity被回收了，变量变成null，
</p>
<p>
	参考下面一篇博客
</p>
<p>
	http://blog.csdn.net/huyongl1989/article/details/49333953
</p>
<p>
	还有三星手机可能会遇到变量空针
</p>
<p>
	需要在AndroidManifest.xml的Activity里加入<br />
	
</p>
<pre style="font-family:Menlo; font-size:12pt; background-color:rgb(255,255,255)"><span style="color:#0000ff; background-color:#e4e4ff"><strong>android</strong></span><span style="color:#0000ff"><strong>:configChanges=</strong></span><span style="color:#008000"><strong>&quot;mcc|mnc|keyboard|keyboardHidden|navigation|orientation|screenSize|fontScale&quot;</strong></span></pre>
<p>
</p>
<p>
	<br />
	
</p>
<p>
	如何在Fragment上调用拍照，图片如何压缩
</p>
<p>
	经过一段时间优化，修复了一些坑。我觉得目前的代码比较可靠，总结一下封装后分享出来。<br />
	
</p>
<p>
	<img src="http://img.blog.csdn.net/20160526181230188" alt="" /><br />
	
</p>
<p>
	<img src="http://img.blog.csdn.net/20160526181247935" alt="" /><br />
	
</p>
<p>
	<br />
	
</p>
<p>
	<img src="http://img.blog.csdn.net/20160526181354608" alt="" /><br />
	
</p>
<p>
	<img src="http://img.blog.csdn.net/20160526181314720" alt="" /><br />
	
</p>
<p>
	<br />
	
</p>
<p>
	<br />
	
</p>
