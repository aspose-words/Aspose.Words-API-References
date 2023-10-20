---
title: CustomDocumentProperties Class
linktitle: CustomDocumentProperties
articleTitle: CustomDocumentProperties
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Properties.CustomDocumentProperties 班级. 自定义文档属性的集合 在 C#.
type: docs
weight: 4460
url: /zh/net/aspose.words.properties/customdocumentproperties/
---
## CustomDocumentProperties class

自定义文档属性的集合。

要了解更多信息，请访问[使用文档属性](https://docs.aspose.com/words/net/work-with-document-properties/)文档文章。

```csharp
public class CustomDocumentProperties : DocumentPropertyCollection
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.properties/documentpropertycollection/count/) { get; } | 获取集合中的项目数。 |
| [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | 返回一个[`DocumentProperty`](../documentproperty/)按索引的对象. |
| virtual [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | 返回一个[`DocumentProperty`](../documentproperty/)对象的属性名称。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add)(*string, bool*) | 创建一个新的自定义文档属性Boolean数据类型. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_3)(*string, DateTime*) | 创建一个新的自定义文档属性DateTime数据类型. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_1)(*string, double*) | 创建一个新的自定义文档属性Double数据类型. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_2)(*string, int*) | 创建一个新的自定义文档属性Number数据类型. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_4)(*string, string*) | 创建一个新的自定义文档属性String数据类型. |
| [AddLinkToContent](../../aspose.words.properties/customdocumentproperties/addlinktocontent/)(*string, string*) | 创建一个新的链接到内容自定义文档属性。 |
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | 从集合中删除所有属性。 |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(*string*) | 返回`真的`如果集合中存在具有指定名称的属性。 |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | 返回一个枚举器对象，可用于迭代集合中的所有项目。 |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(*string*) | 按名称获取属性的索引。 |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(*string*) | 从集合中删除具有指定名称的属性。 |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(*int*) | 删除指定索引处的属性。 |

## 评论

每个[`DocumentProperty`](../documentproperty/)object 表示容器文档的自定义属性。

属性的名称不区分大小写。

集合中的属性按名称字母顺序排序。

## 例子

展示如何使用自定义文档属性。

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// 每个文档都包含自定义属性的集合，这些属性与内置属性一样，都是键值对。
 // 该文档有一个固定的内置属性列表。用户创建所有自定义属性。
Assert.AreEqual("Value of custom document property", doc.CustomDocumentProperties["CustomProperty"].ToString());

doc.CustomDocumentProperties.Add("CustomProperty2", "Value of custom document property #2");

Console.WriteLine("Custom Properties:");
foreach (var customDocumentProperty in doc.CustomDocumentProperties)
{
    Console.WriteLine(customDocumentProperty.Name);
    Console.WriteLine($"\tType:\t{customDocumentProperty.Type}");
    Console.WriteLine($"\tValue:\t\"{customDocumentProperty.Value}\"");
}
```

### 也可以看看

* class [Document](../../aspose.words/document/)
* property [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/)
* property [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/)
* class [DocumentPropertyCollection](../documentpropertycollection/)
* 命名空间 [Aspose.Words.Properties](../../aspose.words.properties/)
* 部件 [Aspose.Words](../../)
