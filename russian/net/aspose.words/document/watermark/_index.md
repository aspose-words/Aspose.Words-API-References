---
title: Document.Watermark
linktitle: Watermark
articleTitle: Watermark
second_title: Aspose.Words для .NET
description: Защитите свои документы с помощью нашей настраиваемой функции водяных знаков. Улучшите защиту и обеспечьте подлинность без усилий!
type: docs
weight: 500
url: /ru/net/aspose.words/document/watermark/
---
## Document.Watermark property

Предоставляет доступ к водяному знаку документа.

```csharp
public Watermark Watermark { get; }
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

* class [Watermark](../../watermark/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
