---
title: TextWatermarkOptions.IsSemitrasparent
second_title: Справочник по API Aspose.Words для .NET
description: TextWatermarkOptions свойство. Получает или задает логическое значение отвечающее за непрозрачность водяного знака. Значение по умолчанию  True.
type: docs
weight: 50
url: /ru/net/aspose.words/textwatermarkoptions/issemitrasparent/
---
## TextWatermarkOptions.IsSemitrasparent property

Получает или задает логическое значение, отвечающее за непрозрачность водяного знака. Значение по умолчанию — True.

```csharp
public bool IsSemitrasparent { get; set; }
```

### Примеры

Показывает, как создать текстовый водяной знак.

```csharp
Document doc = new Document();

// Добавляем простой текстовый водяной знак.
doc.Watermark.SetText("Aspose Watermark");

// Если мы хотим отредактировать форматирование текста, используя его как водяной знак,
// мы можем сделать это, передав объект TextWatermarkOptions при создании водяного знака.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// Мы можем удалить водяной знак из такого документа.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### Смотрите также

* class [TextWatermarkOptions](../)
* пространство имен [Aspose.Words](../../textwatermarkoptions/)
* сборка [Aspose.Words](../../../)


