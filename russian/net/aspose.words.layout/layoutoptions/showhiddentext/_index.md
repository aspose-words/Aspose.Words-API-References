---
title: LayoutOptions.ShowHiddenText
linktitle: ShowHiddenText
articleTitle: ShowHiddenText
second_title: Aspose.Words для .NET
description: Откройте для себя свойство LayoutOptions ShowHiddenText, легко управляйте отображением скрытого текста в ваших документах. Оптимизируйте видимость вашего контента сегодня!
type: docs
weight: 80
url: /ru/net/aspose.words.layout/layoutoptions/showhiddentext/
---
## LayoutOptions.ShowHiddenText property

Возвращает или задает признак того, отображается ли скрытый текст в документе. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ShowHiddenText { get; set; }
```

## Примечания

Это свойство влияет на весь скрытый контент, а не только на текст.

## Примеры

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
* пространство имен [Aspose.Words.Layout](../../../aspose.words.layout/)
* сборка [Aspose.Words](../../../)
