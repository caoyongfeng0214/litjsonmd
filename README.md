该项目是<a href="http://litjson.sourceforge.net/">LitJSON</a>的改进版本。

它可帮助您在.net中对JSON进行处理。

解决了LitJSON原项目中的以下问题：

*空数组的转换问题
*中文显示问题
*类型转换问题
*嵌套数组转换的问题

----

一个简单示例：

<pre>
<code>
  String str = "{'name':'cyf','id':10,'items':[{'itemid':1001,'itemname':'hello'},{'itemid':1002,'itemname':'hello2'}]}";

  //*** 读取JSON字符串中的数据 *******************************
  JsonData jd = JsonMapper.ToObject(str);
  String name = (String)jd["name"];
  long id = (long)jd["id"];
  JsonData jdItems = jd["items"];
  int itemCnt = jdItems.Count; // 数组 items 中项的数量
  foreach (JsonData item in jdItems) // 遍历数组 items
  {
      int itemID = (int)item["itemid"];
      String itemName = (String)item["itemname"];
  }

  //*** 将JsonData转换为JSON字符串 ***************************
  String str2 = jd.ToJson();
  </code>
</pre>

----

参考：<a href="http://www.nooong.com/docs/litjsonmd/">LitJSON_MD 简明文档</a>

本人G+：<a href="http://google.com/+YFCAO">google.com/+YFCAO</a>

Thanks to <a href="http://leonardoboshell.users.sourceforge.net/">Leonardo Boshell</a> 。

若欲了解有关LitJSON的更多内容及文档，请参阅：http://litjson.sourceforge.net/ 。
