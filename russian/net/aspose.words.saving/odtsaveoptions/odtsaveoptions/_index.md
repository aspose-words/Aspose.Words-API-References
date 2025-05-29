---
title: OdtSaveOptions
linktitle: OdtSaveOptions
articleTitle: OdtSaveOptions
second_title: Aspose.Words для .NET
description: Откройте для себя конструктор OdtSaveOptions, чтобы без усилий сохранять документы в формате ODT. Оптимизируйте свой рабочий процесс с помощью этого мощного инструмента!
type: docs
weight: 10
url: /ru/net/aspose.words.saving/odtsaveoptions/odtsaveoptions/
---
## OdtSaveOptions() {#constructor}

Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа вOdt формат.

```csharp
public OdtSaveOptions()
```

## Примеры

Показывает, как привести сохраненный документ в соответствие со старой схемой ODT.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Смотрите также

* class [OdtSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)

---

## OdtSaveOptions(*string*) {#constructor_2}

Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа вOdt format зашифрованный паролем.

```csharp
public OdtSaveOptions(string password)
```

### Смотрите также

* class [OdtSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)

---

## OdtSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа вOdt или Ott формат.

```csharp
public OdtSaveOptions(SaveFormat saveFormat)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormat | SaveFormat | Может бытьOdt илиOtt. |

## Примеры

Показывает, как зашифровать сохраненный документ ODT/OTT с помощью пароля, а затем загрузить его с помощью Aspose.Words.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Создайте новый OdtSaveOptions и передайте либо "SaveFormat.Odt",
 // или "SaveFormat.Ott" в качестве формата для сохранения документа.
OdtSaveOptions saveOptions = new OdtSaveOptions(saveFormat);
saveOptions.Password = "@sposeEncrypted_1145";

string extensionString = FileFormatUtil.SaveFormatToExtension(saveFormat);

// Если мы откроем этот документ с помощью соответствующего редактора,
// он запросит у нас пароль, который мы указали в объекте SaveOptions.
doc.Save(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString, saveOptions);

FileFormatInfo docInfo = FileFormatUtil.DetectFileFormat(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString);

Assert.IsTrue(docInfo.IsEncrypted);

// Если мы хотим снова открыть или отредактировать этот документ с помощью Aspose.Words,
// нам придется предоставить объект LoadOptions с правильным паролем конструктору загрузки.
doc = new Document(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString,
    new LoadOptions("@sposeEncrypted_1145"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OdtSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
