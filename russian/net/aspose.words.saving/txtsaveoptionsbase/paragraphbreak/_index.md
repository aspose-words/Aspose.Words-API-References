---
title: TxtSaveOptionsBase.ParagraphBreak
linktitle: ParagraphBreak
articleTitle: ParagraphBreak
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ParagraphBreak TxtSaveOptionsBase, позволяющее настраивать разрывы абзацев для бесшовного экспорта текстовых форматов. Улучшите читаемость вашего документа!
type: docs
weight: 40
url: /ru/net/aspose.words.saving/txtsaveoptionsbase/paragraphbreak/
---
## TxtSaveOptionsBase.ParagraphBreak property

Указывает строку, которая будет использоваться в качестве разрыва абзаца при экспорте в текстовые форматы.

```csharp
public string ParagraphBreak { get; set; }
```

## Примечания

Значение по умолчанию:[`CrLf`](../../../aspose.words/controlchar/crlf/).

## Примеры

Показывает, как сохранить документ .txt с пользовательским разрывом абзаца.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

// Создаем объект "TxtSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ сохранения документа в виде обычного текста.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

Assert.AreEqual(SaveFormat.Text, txtSaveOptions.SaveFormat);

// Задайте для «ParagraphBreak» пользовательское значение, которое мы хотим поместить в конец каждого абзаца.
txtSaveOptions.ParagraphBreak = " End of paragraph.\n\n\t";

doc.Save(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt");

Assert.AreEqual("Paragraph 1. End of paragraph.\n\n\t" +
                "Paragraph 2. End of paragraph.\n\n\t" +
                "Paragraph 3. End of paragraph.\n\n\t", docText);
```

### Смотрите также

* class [TxtSaveOptionsBase](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
