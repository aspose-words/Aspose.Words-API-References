---
title: WatermarkLayout Enum
linktitle: WatermarkLayout
articleTitle: WatermarkLayout
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.WatermarkLayout для оптимального позиционирования водяного знака. Улучшите дизайн документа с помощью точного управления макетом и настройки.
type: docs
weight: 7530
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
| Horizontal | `0` | Горизонтальное расположение водяного знака. Соответствует 0 градусам поворота. |
| Diagonal | `315` | Диагональное расположение водяного знака. Соответствует повороту на 315 градусов. |

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
