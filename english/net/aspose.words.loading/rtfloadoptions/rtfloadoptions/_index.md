---
title: RtfLoadOptions
linktitle: RtfLoadOptions
articleTitle: RtfLoadOptions
second_title: Aspose.Words for .NET
description: RtfLoadOptions constructor. Initializes a new instance of this class with default values in C#.
type: docs
weight: 10
url: /net/aspose.words.loading/rtfloadoptions/rtfloadoptions/
---
## RtfLoadOptions constructor

Initializes a new instance of this class with default values.

```csharp
public RtfLoadOptions()
```

## Examples

Shows how to detect UTF-8 characters while loading an RTF document.

```csharp
// Create an "RtfLoadOptions" object to modify how we load an RTF document.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// Set the "RecognizeUtf8Text" property to "false" to assume that the document uses the ISO 8859-1 charset
// and loads every character in the document.
// Set the "RecognizeUtf8Text" property to "true" to parse any variable-length characters that may occur in the text.
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

### See Also

* class [RtfLoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
