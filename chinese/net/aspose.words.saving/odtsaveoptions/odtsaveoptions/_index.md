---
title: OdtSaveOptions
linktitle: OdtSaveOptions
articleTitle: OdtSaveOptions
second_title: Aspose.Words for .NET
description: 探索 OdtSaveOptions 构造函数，轻松将文档保存为 ODT 格式。使用这款强大的工具，简化您的工作流程！
type: docs
weight: 10
url: /zh/net/aspose.words.saving/odtsaveoptions/odtsaveoptions/
---
## OdtSaveOptions() {#constructor}

初始化此类的新实例，可用于将文档保存在Odt格式.

```csharp
public OdtSaveOptions()
```

## 例子

展示如何使保存的文档符合旧的 ODT 模式。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### 也可以看看

* class [OdtSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)

---

## OdtSaveOptions(*string*) {#constructor_2}

初始化此类的新实例，可用于将文档保存在Odt format 使用密码加密。

```csharp
public OdtSaveOptions(string password)
```

### 也可以看看

* class [OdtSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)

---

## OdtSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

初始化此类的新实例，可用于将文档保存在Odt或 Ott格式.

```csharp
public OdtSaveOptions(SaveFormat saveFormat)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveFormat | SaveFormat | 可以Odt或者Ott。 |

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OdtSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
