---
title: OdtSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words for .NET
description: 使用 OdtSaveOptions 的密码属性保护您的文档。轻松设置或检索密码，实现强大的加密和增强的数据保护。
type: docs
weight: 50
url: /zh/net/aspose.words.saving/odtsaveoptions/password/
---
## OdtSaveOptions.Password property

获取或设置加密文档的密码。

```csharp
public string Password { get; set; }
```

## 评论

为了在不加密的情况下保存文档，此属性应该是`无效的`或空字符串。

## 例子

展示如何使用密码加密已保存的 ODT/OTT 文档，然后使用 Aspose.Words 加载它。

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

// 如果我们希望使用 Aspose.Words 再次打开或编辑此文档，
// 我们必须向加载构造函数提供具有正确密码的 LoadOptions 对象。
doc = new Document(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString,
    new LoadOptions("@sposeEncrypted_1145"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### 也可以看看

* class [OdtSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
