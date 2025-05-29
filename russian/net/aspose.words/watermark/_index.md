---
title: Watermark Class
linktitle: Watermark
articleTitle: Watermark
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Watermark, который позволит вам легко добавлять и настраивать водяные знаки в ваших документах, повышая профессионализм и брендинг.
type: docs
weight: 7520
url: /ru/net/aspose.words/watermark/
---
## Watermark class

Представляет класс для работы с водяными знаками документа.

Чтобы узнать больше, посетите[Работа с водяным знаком](https://docs.aspose.com/words/net/working-with-watermark/) документальная статья.

```csharp
public sealed class Watermark
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Type](../../aspose.words/watermark/type/) { get; } | Получает тип водяного знака. |

## Методы

| Имя | Описание |
| --- | --- |
| [Remove](../../aspose.words/watermark/remove/)() | Удаляет водяной знак. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage)(*Image*) | Добавляет водяной знак изображения в документ. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_1)(*Image, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Добавляет водяной знак изображения в документ. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_2)(*Stream, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Добавляет водяной знак изображения в документ. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_3)(*string, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Добавляет водяной знак изображения в документ. |
| [SetText](../../aspose.words/watermark/settext/#settext)(*string*) | Добавляет текстовый водяной знак в документ. |
| [SetText](../../aspose.words/watermark/settext/#settext_1)(*string, [TextWatermarkOptions](../textwatermarkoptions/)*) | Добавляет текстовый водяной знак в документ. |

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
