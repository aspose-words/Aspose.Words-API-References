---
title: TextWatermarkOptions Class
linktitle: TextWatermarkOptions
articleTitle: TextWatermarkOptions
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.TextWatermarkOptions для настраиваемых текстовых водяных знаков. Улучшите свои документы с помощью уникальных, профессиональных вариантов брендинга!
type: docs
weight: 7290
url: /ru/net/aspose.words/textwatermarkoptions/
---
## TextWatermarkOptions class

Содержит параметры, которые можно указать при добавлении водяного знака с текстом.

Чтобы узнать больше, посетите[Работа с водяным знаком](https://docs.aspose.com/words/net/working-with-watermark/) документальная статья.

```csharp
public class TextWatermarkOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [TextWatermarkOptions](textwatermarkoptions/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Color](../../aspose.words/textwatermarkoptions/color/) { get; set; } | Получает или задает цвет шрифта. Значение по умолчанию:Silver . |
| [FontFamily](../../aspose.words/textwatermarkoptions/fontfamily/) { get; set; } | Получает или задает имя семейства шрифтов. Значение по умолчанию — «Calibri». |
| [FontSize](../../aspose.words/textwatermarkoptions/fontsize/) { get; set; } | Получает или задает размер шрифта. Значение по умолчанию 0 - auto. |
| [IsSemitrasparent](../../aspose.words/textwatermarkoptions/issemitrasparent/) { get; set; } | Возвращает или задает логическое значение, которое отвечает за непрозрачность водяного знака. Значение по умолчанию:`истинный` . |
| [Layout](../../aspose.words/textwatermarkoptions/layout/) { get; set; } | Получает или задает макет водяного знака. Значение по умолчанию:Diagonal . |

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
