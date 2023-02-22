---
title: LayoutOptions.ShowHiddenText
second_title: Справочник по API Aspose.Words для .NET
description: LayoutOptions свойство. Получает или задает индикацию того визуализируется ли скрытый текст в документе. Значение по умолчанию  False.
type: docs
weight: 70
url: /ru/net/aspose.words.layout/layoutoptions/showhiddentext/
---
## LayoutOptions.ShowHiddenText property

Получает или задает индикацию того, визуализируется ли скрытый текст в документе. Значение по умолчанию — False.

```csharp
public bool ShowHiddenText { get; set; }
```

### Примечания

Это свойство влияет на весь скрытый контент, а не только на текст.

### Примеры

Показывает, как скрыть текст в визуализируемом выходном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Вставляем скрытый текст, затем указываем, хотим ли мы исключить его из визуализируемого документа.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

### Смотрите также

* class [LayoutOptions](../)
* пространство имен [Aspose.Words.Layout](../../layoutoptions/)
* сборка [Aspose.Words](../../../)


