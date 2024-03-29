---
title: WatermarkType Enum
linktitle: WatermarkType
articleTitle: WatermarkType
second_title: Aspose.Words для .NET
description: Aspose.Words.WatermarkType перечисление. Указывает тип водяного знака на С#.
type: docs
weight: 6690
url: /ru/net/aspose.words/watermarktype/
---
## WatermarkType enumeration

Указывает тип водяного знака.

```csharp
public enum WatermarkType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Text | `0` | Указывает, что текст будет использоваться в качестве водяного знака. |
| Image | `1` | Указывает, что изображение будет использоваться в качестве водяного знака. |
| None | `2` | Указывает, что водяной знак не установлен. |

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
