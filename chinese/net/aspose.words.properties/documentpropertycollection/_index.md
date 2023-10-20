---
title: DocumentPropertyCollection Class
linktitle: DocumentPropertyCollection
articleTitle: DocumentPropertyCollection
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Properties.DocumentPropertyCollection 班级. 的基类BuiltInDocumentProperties和CustomDocumentProperties收藏 在 C#.
type: docs
weight: 4480
url: /zh/net/aspose.words.properties/documentpropertycollection/
---
## DocumentPropertyCollection class

的基类[`BuiltInDocumentProperties`](../builtindocumentproperties/)和[`CustomDocumentProperties`](../customdocumentproperties/)收藏.

要了解更多信息，请访问[使用文档属性](https://docs.aspose.com/words/net/work-with-document-properties/)文档文章。

```csharp
public abstract class DocumentPropertyCollection : IEnumerable<DocumentProperty>
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
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | 从集合中删除所有属性。 |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(*string*) | 返回`真的`如果集合中存在具有指定名称的属性。 |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | 返回一个枚举器对象，可用于迭代集合中的所有项目。 |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(*string*) | 按名称获取属性的索引。 |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(*string*) | 从集合中删除具有指定名称的属性。 |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(*int*) | 删除指定索引处的属性。 |

## 评论

属性的名称不区分大小写。

集合中的属性按名称字母顺序排序。

## 例子

展示如何使用文档的自定义属性。

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// 自定义文档属性是我们可以添加到文档中的键值对。
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// 该集合按字母顺序对自定义属性进行排序。
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// 打印文档中的每个自定义属性。
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// 使用 DOCPROPERTY 字段显示自定义属性的值。
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// 我们可以通过“文件”-> 在 Microsoft Word 中找到这些自定义属性“属性”> “高级属性”> “风俗”。
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// 以下是从文档中删除自定义属性的三种方法。
// 1 - 按索引删除：
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - 按名称删除：
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - 立即清空整个集合：
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### 也可以看看

* class [BuiltInDocumentProperties](../builtindocumentproperties/)
* class [CustomDocumentProperties](../customdocumentproperties/)
* class [DocumentProperty](../documentproperty/)
* 命名空间 [Aspose.Words.Properties](../../aspose.words.properties/)
* 部件 [Aspose.Words](../../)
