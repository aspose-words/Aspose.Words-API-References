---
title: RtfLoadOptions
linktitle: RtfLoadOptions
articleTitle: RtfLoadOptions
second_title: Aspose.Words для .NET
description: Откройте для себя конструктор RtfLoadOptions, который легко инициализирует ваш класс значениями по умолчанию, повышая эффективность и производительность кодирования.
type: docs
weight: 10
url: /ru/net/aspose.words.loading/rtfloadoptions/rtfloadoptions/
---
## RtfLoadOptions constructor

Инициализирует новый экземпляр этого класса со значениями по умолчанию.

```csharp
public RtfLoadOptions()
```

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
