---
title: DocumentPropertyCollection.GetEnumerator
second_title: Aspose.Words for .NET API 参考
description: DocumentPropertyCollection 方法. 返回一个枚举器对象可用于迭代集合中的所有项目
type: docs
weight: 50
url: /zh/net/aspose.words.properties/documentpropertycollection/getenumerator/
---
## DocumentPropertyCollection.GetEnumerator method

返回一个枚举器对象，可用于迭代集合中的所有项目。

```csharp
public IEnumerator<DocumentProperty> GetEnumerator()
```

### 例子

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

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* 命名空间 [Aspose.Words.Properties](../../documentpropertycollection/)
* 部件 [Aspose.Words](../../../)


