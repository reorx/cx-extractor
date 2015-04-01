对于Web信息检索来说，网页正文抽取是后续处理的关键。

虽然使用正则表达式可以准确的抽取某一固定格式的页面，但面对形形色色的HTML，使用规则处理难免捉襟见肘。能不能高效、准确的将一个页面的正文抽取出来，并做到在
大规模网页范围内通用，这是一个直接关系上层应用的难题。

[作者](http://weibo.com/cx3180)提出了[《基于行块分布函数的通用网页正文抽取算法》](http://cx-extractor.go
oglecode.com/files/%E5%9F%BA%E4%BA%8E%E8%A1%8C%E5%9D%97%E5%88%86%E5%B8%83%E5%8
7%BD%E6%95%B0%E7%9A%84%E9%80%9A%E7%94%A8%E7%BD%91%E9%A1%B5%E6%AD%A3%E6%96%87%E
6%8A%BD%E5%8F%96%E7%AE%97%E6%B3%95.pdf)，首次将网页正文抽取问题转化为求页面的行块分布函数，这种方法不用建立Dom树，
不被病态HTML所累（事实上与HTML标签完全无关）。通过在线性时间内建立的行块分布函数图，直接准确定位网页正文。同时采用了统计与规则相结合的方法来处理通用
性问题。作者相信简单的事情总应该用最简单的办法来解决这一亘古不变的道理。整个算法实现代码不足百行。但量不在多，在法。

建议使用svn checkout <http://cx-
extractor.googlecode.com/svn/trunk/>，svn的好处是更新及时，zip包作者不能保证每次修改完后都及时上传 **:)**


There are undoubtedly serious bugs lurking somewhere in code this funky. So
feel free to contact us if you meet any problem.
Bug reports and other feedback are most welcome :-)

**Version** |  **Author** |  **Email** |  **Institute**
---|---|---|---
Perl| [陈鑫](http://ir.hit.edu.cn/~xchen)| xchen@ir.hit.edu.cn|[哈工大信息检索研究中心](http://ir.hit.edu.cn)
Java| [王利锋](http://ir.hit.edu.cn/~lfwang)、[罗磊](http://ir.hit.edu.cn/~lluo)|{lfwang,lluo}@ir.hit.edu.cn| [哈工大信息检索研究中心](http://ir.hit.edu.cn)
C++| 朱亮| zhuliang@software.ict.ac.cn| [中科院计算所高级网络重点实验室](http://www.ict.ac.cn)
PHP| 轩文烽| xwf1788@gmail.com| [哈工大智能技术与自然语言处理研究室](http://www.insun.hit.edu.cn)
C#| 张帆| zfannn@gmail.com| [中科院信息科学与工程学院](http://www.gu.cas.cn/yxsz/xxkxygcxy/)


如果您正在关注或使用cx-extractor，同时希望在第一时间得到该项目的更新信息，
您可以加入该项目的邮件列表 http://list.qq.com/cgi-bin/qf_invite?id=2a19dc7f75fcba75ee9962adfcf5013e3154e3b92ef767a3


本软件的使用许可协议:[署名-非商业性使用-相同方式共享 (by-nc-
sa)](http://cn.creativecommons.org/licenses/meet-the-
licenses/)，新浪微博<http://weibo.com/cx3180>

---

建议：

1. 如果要提取娱乐类的网页，尤其是在图片把正文分割的比较支离破碎时，
   建议用Java版代码。Java版实现时对多个正文片段进行合并，可以很好
   的处理这一问题。但缺点是正文结尾可能会有少许噪声。


2. Perl和PHP的实现版本，一遍扫描只求最大行块，不进行拼接。如果出
   现特别支离破碎的正文时，可能会有丢失。但优点是边缘的噪声去除的
   很好。




有任何问题，欢迎随时联系我：）
****************************************
陈  鑫
Email: cx3180@gmail.com
Blog:  http://hi.baidu.com/爱心同盟_陈鑫
****************************************
