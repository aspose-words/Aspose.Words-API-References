---
title: Document.VersionsCount
linktitle: VersionsCount
articleTitle: VersionsCount
second_title: 用于 .NET 的 Aspose.Words
description: Document VersionsCount 财产. 获取 DOC 文档中存储的文档版本数 在 C#.
type: docs
weight: 460
url: /zh/net/aspose.words/document/versionscount/
---
## Document.VersionsCount property

获取 DOC 文档中存储的文档版本数。

```csharp
public int VersionsCount { get; }
```

## 评论

Microsoft Word 中的版本可通过“文件/版本”菜单访问。 Microsoft Word 仅支持 DOC 文件的 版本。

此属性允许检测在 Aspose.Words 中打开此 document 之前是否存储有文档版本。 Aspose.Words 不提供对文档版本的其他支持。 如果您使用 Aspose.Words 保存此文档，则该文档将在没有版本的情况下保存。

## 例子

演示如何使用旧版 Microsoft Word 文档的版本计数功能。

```csharp
Document doc = new Document(MyDir + "Versions.doc");

// 我们可以读取文档的此属性，但无法在保存时保留它。
Assert.AreEqual(4, doc.VersionsCount);

doc.Save(ArtifactsDir + "Document.VersionsCount.doc");      
doc = new Document(ArtifactsDir + "Document.VersionsCount.doc");

Assert.AreEqual(0, doc.VersionsCount);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
