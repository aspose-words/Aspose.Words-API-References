---
title: DocumentProperty.LinkSource
linktitle: LinkSource
articleTitle: LinkSource
second_title: Aspose.Words for .NET
description: 发现 DocumentProperty 的 LinkSource 属性，轻松访问链接的自定义文档属性的源，以增强文档管理。
type: docs
weight: 20
url: /zh/net/aspose.words.properties/documentproperty/linksource/
---
## DocumentProperty.LinkSource property

获取链接自定义文档属性的来源。

```csharp
public string LinkSource { get; }
```

## 例子

展示如何将自定义文档属性链接到书签。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("MyBookmark");
builder.Write("Hello world!");
builder.EndBookmark("MyBookmark");

// 将新的自定义属性链接到书签。此属性的值
// 将是其在“LinkSource”成员中引用的书签的内容。
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
