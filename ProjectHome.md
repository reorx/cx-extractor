对于Web信息检索来说，网页正文抽取是后续处理的关键。

虽然使用正则表达式可以准确的抽取某一固定格式的页面，但面对形形色色的HTML，使用规则处理难免捉襟见肘。能不能高效、准确的将一个页面的正文抽取出来，并做到在大规模网页范围内通用，这是一个直接关系上层应用的难题。

[作者](http://weibo.com/cx3180)提出了[《基于行块分布函数的通用网页正文抽取算法》](http://cx-extractor.googlecode.com/files/%E5%9F%BA%E4%BA%8E%E8%A1%8C%E5%9D%97%E5%88%86%E5%B8%83%E5%87%BD%E6%95%B0%E7%9A%84%E9%80%9A%E7%94%A8%E7%BD%91%E9%A1%B5%E6%AD%A3%E6%96%87%E6%8A%BD%E5%8F%96%E7%AE%97%E6%B3%95.pdf)，首次将网页正文抽取问题转化为求页面的行块分布函数，这种方法不用建立Dom树，不被病态HTML所累（事实上与HTML标签完全无关）。通过在线性时间内建立的行块分布函数图，直接准确定位网页正文。同时采用了统计与规则相结合的方法来处理通用性问题。作者相信简单的事情总应该用最简单的办法来解决这一亘古不变的道理。整个算法实现代码不足百行。但量不在多，在法。

建议使用svn checkout http://cx-extractor.googlecode.com/svn/trunk/，svn的好处是更新及时，zip包作者不能保证每次修改完后都及时上传 **:)**


<br>
There are undoubtedly serious bugs lurking somewhere in code this funky. So feel free to contact us if you meet any problem.<br>
Bug reports and other feedback are most welcome :-)<br>
<table><thead><th> <b>Version</b> </th><th> <b>Author</b> </th><th> <b>Email</b> </th><th> <b>Institute</b> </th></thead><tbody>
<tr><td>Perl</td><td><a href='http://ir.hit.edu.cn/~xchen'>陈鑫</a></td><td>xchen@ir.hit.edu.cn</td><td><a href='http://ir.hit.edu.cn'>哈工大信息检索研究中心</a></td></tr>
<tr><td>Java</td><td><a href='http://ir.hit.edu.cn/~lfwang'>王利锋</a>、<a href='http://ir.hit.edu.cn/~lluo'>罗磊</a></td><td>{lfwang,lluo}@ir.hit.edu.cn</td><td><a href='http://ir.hit.edu.cn'>哈工大信息检索研究中心</a></td></tr>
<tr><td>C++</td><td>朱亮</td><td>zhuliang@software.ict.ac.cn</td><td><a href='http://www.ict.ac.cn'>中科院计算所高级网络重点实验室</a></td></tr>
<tr><td>PHP</td><td>轩文烽</td><td>xwf1788@gmail.com</td><td><a href='http://www.insun.hit.edu.cn'>哈工大智能技术与自然语言处理研究室</a></td></tr>
<tr><td>C#</td><td>张帆</td><td>zfannn@gmail.com</td><td><a href='http://www.gu.cas.cn/yxsz/xxkxygcxy/'>中科院信息科学与工程学院</a></td></tr></tbody></table>

<br>
如果您正在关注或使用cx-extractor，同时希望在第一时间得到该项目的更新信息，<br>您可以加入该项目的邮件列表 <a href='http://list.qq.com/cgi-bin/qf_invite?id=2a19dc7f75fcba75ee9962adfcf5013e3154e3b92ef767a3'>http://list.qq.com/cgi-bin/qf_invite?id=2a19dc7f75fcba75ee9962adfcf5013e3154e3b92ef767a3</a><br><br>

本软件的使用许可协议:<a href='http://cn.creativecommons.org/licenses/meet-the-licenses/'>署名-非商业性使用-相同方式共享 (by-nc-sa)</a>，新浪微博<a href='http://weibo.com/cx3180'>http://weibo.com/cx3180</a>