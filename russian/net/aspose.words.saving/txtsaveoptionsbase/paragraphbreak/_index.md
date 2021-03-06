---
title: ParagraphBreak
second_title: Справочник по API Aspose.Words для .NET
description: Указывает строку используемую в качестве разрыва абзаца при экспорте в текстовые форматы.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/txtsaveoptionsbase/paragraphbreak/
---
## TxtSaveOptionsBase.ParagraphBreak property

Указывает строку, используемую в качестве разрыва абзаца при экспорте в текстовые форматы.

```csharp
public string ParagraphBreak { get; set; }
```

### Примечания

Значение по умолчанию[`CrLf`](../../../aspose.words/controlchar/crlf).

### Примеры

Показывает, как сохранить документ .txt с настраиваемым разрывом абзаца.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

// Создаем объект "TxtSaveOptions", который мы можем передать в метод "Сохранить" документа
// чтобы изменить способ сохранения документа в виде открытого текста.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

Assert.AreEqual(SaveFormat.Text, txtSaveOptions.SaveFormat);

// Установите для «ParagraphBreak» пользовательское значение, которое мы хотим поместить в конце каждого абзаца.
txtSaveOptions.ParagraphBreak = " End of paragraph.\n\n\t";

doc.Save(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt");

Assert.AreEqual("Paragraph 1. End of paragraph.\n\n\t" +
                "Paragraph 2. End of paragraph.\n\n\t" +
                "Paragraph 3. End of paragraph.\n\n\t", docText);
```

### Смотрите также

* class [TxtSaveOptionsBase](../../txtsaveoptionsbase)
* пространство имен [Aspose.Words.Saving](../../txtsaveoptionsbase)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
