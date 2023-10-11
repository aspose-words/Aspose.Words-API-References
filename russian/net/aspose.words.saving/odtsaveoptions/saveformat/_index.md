---
title: OdtSaveOptions.SaveFormat
second_title: Справочник по API Aspose.Words для .NET
description: OdtSaveOptions свойство. Указывает формат в котором документ будет сохранен если используется этот объект параметров сохранения. Может бытьOdt илиOtt .
type: docs
weight: 50
url: /ru/net/aspose.words.saving/odtsaveoptions/saveformat/
---
## OdtSaveOptions.SaveFormat property

Указывает формат, в котором документ будет сохранен, если используется этот объект параметров сохранения. Может бытьOdt илиOtt .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

### Примеры

Показывает, как зашифровать сохраненный документ ODT/OTT с помощью пароля, а затем загрузить его с помощью Aspose.Words.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Создайте новый OdtSaveOptions и передайте либо "SaveFormat.Odt",
 // или «SaveFormat.Ott» в качестве формата сохранения документа.
OdtSaveOptions saveOptions = new OdtSaveOptions(saveFormat);
saveOptions.Password = "@sposeEncrypted_1145";

string extensionString = FileFormatUtil.SaveFormatToExtension(saveFormat);

// Если мы откроем этот документ в соответствующем редакторе,
// он запросит у нас пароль, который мы указали в объекте SaveOptions.
doc.Save(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString, saveOptions);

FileFormatInfo docInfo = FileFormatUtil.DetectFileFormat(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString);

Assert.IsTrue(docInfo.IsEncrypted);

// Если мы хотим снова открыть или отредактировать этот документ с помощью Aspose.Words,
// нам нужно будет предоставить объект LoadOptions с правильным паролем конструктору загрузки.
doc = new Document(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString,
    new LoadOptions("@sposeEncrypted_1145"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OdtSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../odtsaveoptions/)
* сборка [Aspose.Words](../../../)


