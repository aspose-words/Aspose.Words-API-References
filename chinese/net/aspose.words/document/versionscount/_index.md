---
title: Document.VersionsCount
linktitle: VersionsCount
articleTitle: VersionsCount
second_title: Aspose.Words for .NET
description: 发现文档版本计数属性，轻松跟踪 DOC 文件中存储的文档版本数，以便更好地管理和组织。
type: docs
weight: 480
url: /zh/net/aspose.words/document/versionscount/
---
## Document.VersionsCount property

获取 DOC 文档中存储的文档版本数。

```csharp
public int VersionsCount { get; }
```

## 评论

Microsoft Word 中的版本可通过“文件/版本”菜单访问。Microsoft Word 仅支持 DOC 文件的 x000d 版本。

此属性用于检测此文档 在 Aspose.Words 中打开之前是否存储了文档版本。Aspose.Words 不提供任何其他文档版本支持。 如果您使用 Aspose.Words 保存此文档，则保存的文档将不包含版本信息。

## 例子

展示如何使用旧版 Microsoft Word 文档的版本计数功能。

```csharp
Document doc = new Document(MyDir + "Versions.doc");

// 我们可以读取文档的这个属性，但在保存时无法保留它。
Assert.AreEqual(4, doc.VersionsCount);

doc.Save(ArtifactsDir + "Document.VersionsCount.doc");
doc = new Document(ArtifactsDir + "Document.VersionsCount.doc");

Assert.AreEqual(0, doc.VersionsCount);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
