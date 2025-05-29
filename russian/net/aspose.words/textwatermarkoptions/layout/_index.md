---
title: TextWatermarkOptions.Layout
linktitle: Layout
articleTitle: Layout
second_title: Aspose.Words для .NET
description: Откройте для себя свойство TextWatermarkOptions Layout, чтобы настроить внешний вид вашего водяного знака. Легко установите его на Diagonal или предпочитаемый вами макет для улучшения визуальных эффектов.
type: docs
weight: 60
url: /ru/net/aspose.words/textwatermarkoptions/layout/
---
## TextWatermarkOptions.Layout property

Получает или задает макет водяного знака. Значение по умолчанию:Diagonal .

```csharp
public WatermarkLayout Layout { get; set; }
```

## Примеры

Показывает, как создать текстовый водяной знак.

```csharp
Document doc = new Document();

// Добавить простой текстовый водяной знак.
doc.Watermark.SetText("Aspose Watermark");

// Если мы хотим изменить форматирование текста, используя его как водяной знак,
// мы можем сделать это, передав объект TextWatermarkOptions при создании водяного знака.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// Мы можем удалить водяной знак из документа следующим образом.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### Смотрите также

* enum [WatermarkLayout](../../watermarklayout/)
* class [TextWatermarkOptions](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
