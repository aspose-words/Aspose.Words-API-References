---
title: OdtSaveOptions.SaveFormat
second_title: Aspose.Words for .NET API 参考
description: OdtSaveOptions 财产. 指定使用此保存选项对象时保存文档的格式 可以Odt或者Ott.
type: docs
weight: 50
url: /zh/net/aspose.words.saving/odtsaveoptions/saveformat/
---
## OdtSaveOptions.SaveFormat property

指定使用此保存选项对象时保存文档的格式。 可以Odt或者Ott.

```csharp
public override SaveFormat SaveFormat { get; set; }
```

### 例子

演示如何使用密码加密保存的 ODT/OTT 文档，然后使用 Aspose.Words 加载它。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// 创建一个新的 OdtSaveOptions，并传递“SaveFormat.Odt”，
 // 或“SaveFormat.Ott”作为保存文档的格式。
OdtSaveOptions saveOptions = new OdtSaveOptions(saveFormat);
saveOptions.Password = "@sposeEncrypted_1145";

string extensionString = FileFormatUtil.SaveFormatToExtension(saveFormat);

// 如果我们使用适当的编辑器打开此文档，
// 它将提示我们输入在 SaveOptions 对象中指定的密码。
doc.Save(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString, saveOptions);

FileFormatInfo docInfo = FileFormatUtil.DetectFileFormat(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString);

Assert.IsTrue(docInfo.IsEncrypted);

// 如果我们希望使用 Aspose.Words 再次打开或编辑此文档，
// 我们必须向加载构造函数提供带有正确密码的 LoadOptions 对象。
doc = new Document(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString,
    new LoadOptions("@sposeEncrypted_1145"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OdtSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../odtsaveoptions/)
* 部件 [Aspose.Words](../../../)


