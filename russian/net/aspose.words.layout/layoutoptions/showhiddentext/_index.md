---
title: LayoutOptions.ShowHiddenText
second_title: Справочник по API Aspose.Words для .NET
description: LayoutOptions свойство. Получает или задает индикатор того отображается ли скрытый текст в документе. Значение по умолчаниюЛОЖЬ .
type: docs
weight: 80
url: /ru/net/aspose.words.layout/layoutoptions/showhiddentext/
---
## LayoutOptions.ShowHiddenText property

Получает или задает индикатор того, отображается ли скрытый текст в документе. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ShowHiddenText { get; set; }
```

### Примечания

Это свойство влияет на весь скрытый контент, а не только на текст.

### Примеры

Показывает, как скрыть текст в визуализированном выходном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Вставляем скрытый текст, затем указываем, хотим ли мы исключить его из отображаемого документа.
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


