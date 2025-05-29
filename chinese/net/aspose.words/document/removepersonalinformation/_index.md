---
title: Document.RemovePersonalInformation
linktitle: RemovePersonalInformation
articleTitle: RemovePersonalInformation
second_title: Aspose.Words for .NET
description: 使用 Word 中的文档删除个人信息功能确保隐私，保存时自动从注释和属性中删除用户数据。
type: docs
weight: 360
url: /zh/net/aspose.words/document/removepersonalinformation/
---
## Document.RemovePersonalInformation property

获取或设置一个标志，指示 Microsoft Word 将在保存文档时从注释、修订和文档属性中删除所有用户信息。

```csharp
public bool RemovePersonalInformation { get; set; }
```

## 例子

展示如何在手动保存期间删除个人信息。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一些包含个人信息的内容。
doc.BuiltInDocumentProperties.Author = "John Doe";
doc.BuiltInDocumentProperties.Company = "Placeholder Inc.";

doc.StartTrackRevisions(doc.BuiltInDocumentProperties.Author, DateTime.Now);
builder.Write("Hello world!");
doc.StopTrackRevisions();

// 此标志等同于文件 -> 选项 -> 信任中心 -> 信任中心设置... ->
// 隐私选项 -> Microsoft Word 中的“保存时从文件属性中删除个人信息”。
doc.RemovePersonalInformation = saveWithoutPersonalInfo;

// 使用 Aspose.Words 进行保存操作时此选项不会生效。
// 当我们使用 Microsoft Word 手动保存文档时，个人数据将从文档中删除，并设置标志。
doc.Save(ArtifactsDir + "Document.RemovePersonalInformation.docx");
doc = new Document(ArtifactsDir + "Document.RemovePersonalInformation.docx");

Assert.AreEqual(saveWithoutPersonalInfo, doc.RemovePersonalInformation);
Assert.AreEqual("John Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Placeholder Inc.", doc.BuiltInDocumentProperties.Company);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
