---
title: OoxmlSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words for .NET
description: 使用 OoxmlSaveOptions 保护您的文档！轻松使用 ECMA376 标准设置加密密码，增强数据保护。
type: docs
weight: 60
url: /zh/net/aspose.words.saving/ooxmlsaveoptions/password/
---
## OoxmlSaveOptions.Password property

获取/设置使用 ECMA376 标准加密算法加密文档的密码。

```csharp
public string Password { get; set; }
```

## 评论

为了在不加密的情况下保存文档，此属性应该是`无效的`或空字符串。

## 例子

展示如何创建密码加密的 Office Open XML 文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Password.docx", saveOptions);

// 我们将无法使用 Microsoft Word 或
// Aspose.Words 未提供正确的密码。
Assert.Throws<IncorrectPasswordException>(() =>
    doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx"));

// 通过在 LoadOptions 对象中传递正确的密码来打开加密文档。
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx", new LoadOptions("MyPassword"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### 也可以看看

* class [OoxmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
