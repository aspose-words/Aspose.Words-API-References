---
title: Watermark.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Watermark Type, чтобы улучшить свой дизайн с помощью настраиваемых водяных знаков для брендинга и защиты. Поднимите свои визуальные эффекты сегодня!
type: docs
weight: 10
url: /ru/net/aspose.words/watermark/type/
---
## Watermark.Type property

Получает тип водяного знака.

```csharp
public WatermarkType Type { get; }
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

* enum [WatermarkType](../../watermarktype/)
* class [Watermark](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
