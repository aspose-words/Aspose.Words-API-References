---
title: RtfLoadOptions.RecognizeUtf8Text
linktitle: RecognizeUtf8Text
articleTitle: RecognizeUtf8Text
second_title: Aspose.Words for .NET
description: Discover how the RtfLoadOptions RecognizeUtf8Text property preserves UTF-8 characters during import, ensuring accurate text representation and seamless integration.
type: docs
weight: 20
url: /net/aspose.words.loading/rtfloadoptions/recognizeutf8text/
---
## RtfLoadOptions.RecognizeUtf8Text property

When set to `true`, will try to detect UTF8 characters, they will be preserved during import.

```csharp
public bool RecognizeUtf8Text { get; set; }
```

## Remarks

Default value is `false`.

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

Assert.That(doc.FirstSection.Body.GetText().Trim(), Is.EqualTo(recognizeUtf8Text
        ? "“John Doe´s list of currency symbols”™\r" +
          "€, ¢, £, ¥, ¤"
        : "â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r" +
          "â‚¬, Â¢, Â£, Â¥, Â¤"));
```

### See Also

* class [RtfLoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
