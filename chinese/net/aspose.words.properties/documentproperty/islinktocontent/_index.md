---
title: DocumentProperty.IsLinkToContent
linktitle: IsLinkToContent
articleTitle: IsLinkToContent
second_title: 用于 .NET 的 Aspose.Words
description: DocumentProperty IsLinkToContent 财产. 显示此属性是否链接到内容 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.properties/documentproperty/islinktocontent/
---
## DocumentProperty.IsLinkToContent property

显示此属性是否链接到内容。

```csharp
public bool IsLinkToContent { get; }
```

## 例子

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

* class [DocumentProperty](../)
* 命名空间 [Aspose.Words.Properties](../../../aspose.words.properties/)
* 部件 [Aspose.Words](../../../)
