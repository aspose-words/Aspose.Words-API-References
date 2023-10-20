---
title: OdtSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: 用于 .NET 的 Aspose.Words
description: OdtSaveOptions Password 财产. 获取或设置密码以加密文档 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.saving/odtsaveoptions/password/
---
## OdtSaveOptions.Password property

获取或设置密码以加密文档。

```csharp
public string Password { get; set; }
```

## 评论

为了在不加密的情况下保存文档，此属性应为 null 或空字符串。

## 例子

展示如何使用密码加密保存的 ODT/OTT 文档，然后使用 Aspose.Words 加载它。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// 创建一个新的 OdtSaveOptions，并传递“SaveFormat.Odt”，
// 或“SaveFormat.Ott”作为保存文档的格式。 
OdtSaveOptions saveOptions = new OdtSaveOptions(saveFormat);
saveOptions.Password = "@sposeEncrypted_1145";

string extensionString = FileFormatUtil.SaveFormatToExtension(saveFormat);

// 如果我们用合适的编辑器打开这个文档，
// 它将提示我们输入在 SaveOptions 对象中指定的密码。
doc.Save(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString, saveOptions);

FileFormatInfo docInfo = FileFormatUtil.DetectFileFormat(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString);

Assert.IsTrue(docInfo.IsEncrypted);

// 如果我们希望再次使用 Aspose.Words 打开或编辑此文档，
// 我们必须为加载构造函数提供一个带有正确密码的 LoadOptions 对象。
doc = new Document(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString,
    new LoadOptions("@sposeEncrypted_1145"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### 也可以看看

* class [OdtSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
