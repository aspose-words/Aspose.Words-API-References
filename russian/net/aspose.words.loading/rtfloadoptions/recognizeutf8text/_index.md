---
title: RtfLoadOptions.RecognizeUtf8Text
second_title: Справочник по API Aspose.Words для .NET
description: RtfLoadOptions свойство. Если установлено значение trueCharsetDetectorпопытается обнаружить символы UTF8 они будут сохранены при импорте.
type: docs
weight: 20
url: /ru/net/aspose.words.loading/rtfloadoptions/recognizeutf8text/
---
## RtfLoadOptions.RecognizeUtf8Text property

Если установлено значение true,CharsetDetectorпопытается обнаружить символы UTF8, они будут сохранены при импорте.

Значение по умолчанию — false.

```csharp
public bool RecognizeUtf8Text { get; set; }
```

### Примеры

Показывает, как обнаруживать символы UTF-8 при загрузке документа RTF.

```csharp
// Создайте объект «RtfLoadOptions», чтобы изменить способ загрузки RTF-документа.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// Установите для свойства "RecognizeUtf8Text" значение "false", чтобы предположить, что документ использует кодировку ISO 8859-1
// и загружает каждый символ в документе.
// Установите для свойства "RecognizeUtf8Text" значение "true", чтобы анализировать любые символы переменной длины, которые могут встречаться в тексте.
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
* пространство имен [Aspose.Words.Loading](../../rtfloadoptions/)
* сборка [Aspose.Words](../../../)


