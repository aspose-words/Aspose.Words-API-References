---
title: DocumentPropertyCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words for .NET
description: 使用 RemoveAt 方法删除任意索引处的属性，轻松管理 DocumentPropertyCollection。立即简化您的文档管理！
type: docs
weight: 80
url: /zh/net/aspose.words.properties/documentpropertycollection/removeat/
---
## DocumentPropertyCollection.RemoveAt method

删除指定索引处的属性。

```csharp
public void RemoveAt(int index)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | Int32 | 从零开始的索引。 |

## 例子

展示如何使用文档的自定义属性。

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// 自定义文档属性是我们可以添加到文档的键值对。
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

// 我们可以在 Microsoft Word 中通过“文件”->“属性”->“高级属性”->“自定义”找到这些自定义属性。
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

// 3 - 一次清空整个集合：
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### 也可以看看

* class [DocumentPropertyCollection](../)
* 命名空间 [Aspose.Words.Properties](../../../aspose.words.properties/)
* 部件 [Aspose.Words](../../../)
