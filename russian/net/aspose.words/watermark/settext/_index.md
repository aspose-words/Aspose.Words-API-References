---
title: Watermark.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words для .NET
description: Улучшите свои документы с помощью нашего метода Watermark SetText. Легко добавляйте настраиваемые текстовые водяные знаки для придания профессионального вида!
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
| text | String | Текст, отображаемый как водяной знак. |

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentOutOfRangeException | Вызывается, когда длина текста выходит за пределы диапазона или текст содержит только пробелы. |
| ArgumentNullException | Выдает, когда текст`нулевой` . |

## Примечания

Длина текста должна быть в диапазоне от 1 до 200 включительно. Текст не может быть`нулевой` или содержать только пробелы.

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
| text | String | Текст, отображаемый как водяной знак. |
| options | TextWatermarkOptions | Определяет дополнительные параметры текстового водяного знака. |

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentOutOfRangeException | Вызывается, когда длина текста выходит за пределы диапазона или текст содержит только пробелы. |
| ArgumentNullException | Выдает, когда текст`нулевой` . |

## Примечания

Длина текста должна быть в диапазоне от 1 до 200 включительно. Текст не может быть`нулевой` или содержать только пробелы.

Если[`TextWatermarkOptions`](../../textwatermarkoptions/) является`нулевой`, водяной знак будет установлен с параметрами по умолчанию.

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

* class [TextWatermarkOptions](../../textwatermarkoptions/)
* class [Watermark](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
