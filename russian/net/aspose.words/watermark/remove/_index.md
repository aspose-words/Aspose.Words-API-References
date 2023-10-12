---
title: Watermark.Remove
second_title: Справочник по API Aspose.Words для .NET
description: Watermark метод. Удаляет водяной знак.
type: docs
weight: 20
url: /ru/net/aspose.words/watermark/remove/
---
## Watermark.Remove method

Удаляет водяной знак.

```csharp
public void Remove()
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

* class [Watermark](../)
* пространство имен [Aspose.Words](../../watermark/)
* сборка [Aspose.Words](../../../)


