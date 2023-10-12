---
title: OdtSaveOptions.Password
second_title: Справочник по API Aspose.Words для .NET
description: OdtSaveOptions свойство. Получает или задает пароль для шифрования документа.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/odtsaveoptions/password/
---
## OdtSaveOptions.Password property

Получает или задает пароль для шифрования документа.

```csharp
public string Password { get; set; }
```

### Примечания

Чтобы сохранить документ без шифрования, это свойство должно быть`нулевой` или пустая строка.

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

* class [OdtSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../odtsaveoptions/)
* сборка [Aspose.Words](../../../)


