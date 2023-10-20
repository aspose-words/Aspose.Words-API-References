---
title: RtfLoadOptions.RecognizeUtf8Text
linktitle: RecognizeUtf8Text
articleTitle: RecognizeUtf8Text
second_title: Aspose.Words для .NET
description: RtfLoadOptions RecognizeUtf8Text свойство. Если установлено значениеистинный CharsetDetector попытается обнаружить символы UTF8 они сохранятся во время импорта на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.loading/rtfloadoptions/recognizeutf8text/
---
## RtfLoadOptions.RecognizeUtf8Text property

Если установлено значение`истинный` ,CharsetDetector попытается обнаружить символы UTF8, они сохранятся во время импорта.

Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool RecognizeUtf8Text { get; set; }
```

## Примеры

Показывает, как обнаружить символы UTF-8 при загрузке документа RTF.

```csharp
// Создайте объект «RtfLoadOptions», чтобы изменить способ загрузки документа RTF.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// Установите для свойства RecounceeUtf8Text значение «false», чтобы предположить, что в документе используется кодировка ISO 8859-1.
// и загружает каждый символ в документе.
// Установите для свойства RecounceeUtf8Text значение «true», чтобы проанализировать любые символы переменной длины, которые могут встретиться в тексте.
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
