---
title: TextWatermarkOptions.Layout
second_title: Справочник по API Aspose.Words для .NET
description: TextWatermarkOptions свойство. Получает или задает макет водяного знака. Значение по умолчаниюDiagonal .
type: docs
weight: 60
url: /ru/net/aspose.words/textwatermarkoptions/layout/
---
## TextWatermarkOptions.Layout property

Получает или задает макет водяного знака. Значение по умолчанию:Diagonal .

```csharp
public WatermarkLayout Layout { get; set; }
```

### Примеры

Показывает, как создать текстовый водяной знак.

```csharp
Document doc = new Document();

// Добавляем простой текстовый водяной знак.
doc.Watermark.SetText("Aspose Watermark");

// Если мы хотим отредактировать форматирование текста, используя его в качестве водяного знака,
// мы можем сделать это, передав объект TextWatermarkOptions при создании водяного знака.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// Мы можем удалить водяной знак из документа вот так.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### Смотрите также

* enum [WatermarkLayout](../../watermarklayout/)
* class [TextWatermarkOptions](../)
* пространство имен [Aspose.Words](../../textwatermarkoptions/)
* сборка [Aspose.Words](../../../)


