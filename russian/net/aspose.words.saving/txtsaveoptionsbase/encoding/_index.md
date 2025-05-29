---
title: TxtSaveOptionsBase.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words для .NET
description: Узнайте, как оптимизировать экспорт текста с помощью свойства кодировки TxtSaveOptionsBase. Легко устанавливайте параметры кодировки для бесшовного форматирования текста UTF-8.
type: docs
weight: 10
url: /ru/net/aspose.words.saving/txtsaveoptionsbase/encoding/
---
## TxtSaveOptionsBase.Encoding property

Указывает кодировку, используемую при экспорте в текстовые форматы. Значение по умолчанию:**Кодировка.UTF8** .

```csharp
public Encoding Encoding { get; set; }
```

## Примеры

Показывает, как задать кодировку для выходного документа .txt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавьте текст с символами, не входящими в набор символов ASCII.
builder.Write("À È Ì Ò Ù.");

// Создаем объект "TxtSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ сохранения документа в виде обычного текста.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Проверяем, что свойство «Кодировка» содержит соответствующую кодировку для содержимого нашего документа.
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

* class [TxtSaveOptionsBase](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
