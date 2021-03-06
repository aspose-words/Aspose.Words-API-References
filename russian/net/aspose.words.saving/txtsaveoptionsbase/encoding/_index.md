---
title: Encoding
second_title: Справочник по API Aspose.Words для .NET
description: Указывает кодировку используемую при экспорте в текстовые форматы. Значение по умолчанию Кодировка.UTF8 .
type: docs
weight: 10
url: /ru/net/aspose.words.saving/txtsaveoptionsbase/encoding/
---
## TxtSaveOptionsBase.Encoding property

Указывает кодировку, используемую при экспорте в текстовые форматы. Значение по умолчанию: **Кодировка.UTF8** .

```csharp
public Encoding Encoding { get; set; }
```

### Примеры

Показывает, как установить кодировку для выходного документа .txt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавляем текст с символами вне набора символов ASCII.
builder.Write("À È Ì Ò Ù.");

// Создаем объект "TxtSaveOptions", который мы можем передать в метод "Сохранить" документа
// чтобы изменить способ сохранения документа в виде открытого текста.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Проверяем, что свойство "Кодировка" содержит соответствующую кодировку для содержимого нашего документа.
Assert.AreEqual(System.Text.Encoding.UTF8, txtSaveOptions.Encoding);

doc.Save(ArtifactsDir + "TxtSaveOptions.Encoding.UTF8.txt", txtSaveOptions);

string docText = System.Text.Encoding.UTF8.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.Encoding.UTF8.txt"));

Assert.AreEqual("\uFEFFÀ È Ì Ò Ù.\r\n", docText);

// Использование неподходящей кодировки может привести к потере содержимого документа.
txtSaveOptions.Encoding = System.Text.Encoding.ASCII;
doc.Save(ArtifactsDir + "TxtSaveOptions.Encoding.ASCII.txt", txtSaveOptions);
docText = System.Text.Encoding.ASCII.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.Encoding.ASCII.txt"));

Assert.AreEqual("? ? ? ? ?.\r\n", docText);
```

### Смотрите также

* class [TxtSaveOptionsBase](../../txtsaveoptionsbase)
* пространство имен [Aspose.Words.Saving](../../txtsaveoptionsbase)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
