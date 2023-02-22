---
title: Enum WatermarkLayout
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.WatermarkLayout перечисление. Определяет расположение водяного знака относительно центра водяного знака.
type: docs
weight: 6370
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
| Horizontal | `0` | Горизонтальное расположение водяных знаков. Соответствует 0 градусов вращения. |
| Diagonal | `315` | Диагональное расположение водяных знаков. Соответствует 315 градусам вращения. |

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


