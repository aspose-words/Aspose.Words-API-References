---
title: WatermarkType Enum
linktitle: WatermarkType
articleTitle: WatermarkType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.WatermarkType для легкой настройки водяных знаков в документах. Улучшите свои проекты с помощью универсальных опций водяных знаков!
type: docs
weight: 7540
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
