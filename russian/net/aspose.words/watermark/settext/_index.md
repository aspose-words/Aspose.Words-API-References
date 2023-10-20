---
title: Watermark.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words для .NET
description: Watermark SetText метод. Добавляет текстовый водяной знак в документ на С#.
type: docs
weight: 40
url: /ru/net/aspose.words/watermark/settext/
---
## SetText(*string*) {#settext}

Добавляет текстовый водяной знак в документ.

```csharp
public void SetText(string text)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| text | String | Текст, отображаемый в виде водяного знака. |

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentOutOfRangeException | Выдается, когда длина текста выходит за пределы допустимого диапазона или текст содержит только пробелы. |
| ArgumentNullException | Выдает, когда текст`нулевой` . |

## Примечания

Длина текста должна быть в диапазоне от 1 до 200 включительно. Текст не может быть`нулевой` или содержать только пробелы.

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

* class [Watermark](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## SetText(*string, [TextWatermarkOptions](../../textwatermarkoptions/)*) {#settext_1}

Добавляет текстовый водяной знак в документ.

```csharp
public void SetText(string text, TextWatermarkOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| text | String | Текст, отображаемый в виде водяного знака. |
| options | TextWatermarkOptions | Определяет дополнительные параметры для текстового водяного знака. |

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentOutOfRangeException | Выдается, когда длина текста выходит за пределы допустимого диапазона или текст содержит только пробелы. |
| ArgumentNullException | Выдает, когда текст`нулевой` . |

## Примечания

Длина текста должна быть в диапазоне от 1 до 200 включительно. Текст не может быть`нулевой` или содержать только пробелы.

Если[`TextWatermarkOptions`](../../textwatermarkoptions/) является`нулевой`, для водяного знака будут установлены параметры по умолчанию.

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

* class [TextWatermarkOptions](../../textwatermarkoptions/)
* class [Watermark](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
