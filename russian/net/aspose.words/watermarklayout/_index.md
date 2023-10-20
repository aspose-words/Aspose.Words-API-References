---
title: WatermarkLayout Enum
linktitle: WatermarkLayout
articleTitle: WatermarkLayout
second_title: Aspose.Words для .NET
description: Aspose.Words.WatermarkLayout перечисление. Определяет расположение водяного знака относительно центра водяного знака на С#.
type: docs
weight: 6680
url: /ru/net/aspose.words/watermarklayout/
---
## WatermarkLayout enumeration

Определяет расположение водяного знака относительно центра водяного знака.

```csharp
public enum WatermarkLayout
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Horizontal | `0` | Горизонтальное расположение водяных знаков. Соответствует 0 градусам вращения. |
| Diagonal | `315` | Расположение водяных знаков по диагонали. Соответствует повороту на 315 градусов. |

## Примеры

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
