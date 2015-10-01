该项目是[LitJSON](http://litjson.sourceforge.net/)的改进版本。

它可帮助您在.net中对JSON进行处理。

解决了[LitJSON](http://litjson.sourceforge.net/)原项目中的以下问题：
  * 空数组的转换问题
  * 中文显示问题
  * 类型转换问题
  * 嵌套数组转换的问题

若您有任何问题，可在此[留言（Post Your Comment）](http://code.google.com/p/litjsonmd/wiki/description)。


---


一个简单示例：

```
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
```

参考：[LitJSON\_MD 简明文档](http://cdn2.nooong.com/litjsonmd/index.htm)<br />
本人G+：[google.com/+YFCAO](http://google.com/+YFCAO)


---


Thanks to [Leonardo Boshell](http://leonardoboshell.users.sourceforge.net/) 。

若欲了解有关LitJSON的更多内容及文档，请参阅：http://litjson.sourceforge.net/ 。