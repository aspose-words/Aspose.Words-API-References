---
title: OoxmlSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: 用于 .NET 的 Aspose.Words
description: OoxmlSaveOptions Password 财产. 获取/设置密码以使用 ECMA376 标准加密算法加密文档 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words.saving/ooxmlsaveoptions/password/
---
## OoxmlSaveOptions.Password property

获取/设置密码以使用 ECMA376 标准加密算法加密文档。

```csharp
public string Password { get; set; }
```

## 评论

为了在不加密的情况下保存文档，此属性应为 null 或空字符串。

## 例子

演示如何创建密码加密的 Office Open XML 文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Password.docx", saveOptions);

// 我们将无法使用 Microsoft Word 或
// Aspose.Words 没有提供正确的密码。
Assert.Throws<IncorrectPasswordException>(() =>
    doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx"));

// 通过在 LoadOptions 对象中传递正确的密码来打开加密的文档。
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx", new LoadOptions("MyPassword"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### 也可以看看

* class [OoxmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
