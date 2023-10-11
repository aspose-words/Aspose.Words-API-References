---
title: CustomDocumentProperties.AddLinkToContent
second_title: Aspose.Words for .NET API 参考
description: CustomDocumentProperties 方法. 创建一个新的链接到内容自定义文档属性
type: docs
weight: 20
url: /zh/net/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties.AddLinkToContent method

创建一个新的链接到内容自定义文档属性。

```csharp
public DocumentProperty AddLinkToContent(string name, string linkSource)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | String | 属性的名称。 |
| linkSource | String | 财产来源。 |

### 返回值

新创建的属性对象或`无效的`当。。。的时候*linkSource*是无效的。

### 例子

演示如何将自定义文档属性链接到书签。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("MyBookmark");
builder.Write("Hello world!");
builder.EndBookmark("MyBookmark");

// 将新的自定义属性链接到书签。该房产的价值
// 将是它在“LinkSource”成员中引用的书签的内容。
CustomDocumentProperties customProperties = doc.CustomDocumentProperties;
DocumentProperty customProperty = customProperties.AddLinkToContent("Bookmark", "MyBookmark");

Assert.AreEqual(true, customProperty.IsLinkToContent);
Assert.AreEqual("MyBookmark", customProperty.LinkSource);
Assert.AreEqual("Hello world!", customProperty.Value);

doc.Save(ArtifactsDir + "DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

### 也可以看看

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* 命名空间 [Aspose.Words.Properties](../../customdocumentproperties/)
* 部件 [Aspose.Words](../../../)


