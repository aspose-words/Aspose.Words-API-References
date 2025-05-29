---
title: RtfLoadOptions.RecognizeUtf8Text
linktitle: RecognizeUtf8Text
articleTitle: RecognizeUtf8Text
second_title: Aspose.Words для .NET
description: Узнайте, как свойство RtfLoadOptions RecognizeUtf8Text сохраняет символы UTF-8 во время импорта, обеспечивая точное представление текста и бесшовную интеграцию.
type: docs
weight: 20
url: /ru/net/aspose.words.loading/rtfloadoptions/recognizeutf8text/
---
## RtfLoadOptions.RecognizeUtf8Text property

При установке на`истинный` , попытается обнаружить символы UTF8, они будут сохранены во время импорта.

```csharp
public bool RecognizeUtf8Text { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ`.

## Примеры

Показывает, как обнаружить символы UTF-8 при загрузке документа RTF.

```csharp
// Создаем объект «RtfLoadOptions» для изменения способа загрузки документа RTF.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// Установите свойство "RecognizeUtf8Text" в значение "false", чтобы предположить, что документ использует кодировку ISO 8859-1
// и загружает каждый символ в документе.
// Установите свойство «RecognizeUtf8Text» в значение «true», чтобы анализировать любые символы переменной длины, которые могут встречаться в тексте.
loadOptions.RecognizeUtf8Text = recognizeUtf8Text;

Document doc = new Document(MyDir + "UTF-8 characters.rtf", loadOptions);

Assert.AreEqual(
    recognizeUtf8Text
        ? "“John Doe´s list of currency symbols”™\r" +
          "€, ¢, £, ¥, ¤"
        : "â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r" +
          "â‚¬, Â¢, Â£, Â¥, Â¤",
    doc.FirstSection.Body.GetText().Trim());
```

### Смотрите также

* class [RtfLoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
