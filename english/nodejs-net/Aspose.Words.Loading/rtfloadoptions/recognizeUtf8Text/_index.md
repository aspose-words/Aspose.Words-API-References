---
title: RtfLoadOptions.recognizeUtf8Text property
linktitle: recognizeUtf8Text property
articleTitle: recognizeUtf8Text property
second_title: Aspose.Words for NodeJs
description: "RtfLoadOptions.recognizeUtf8Text property. When set to ``true``,  will try to detect UTF8 characters,  they will be preserved during import."
type: docs
weight: 20
url: /nodejs-net/aspose.words.loading/rtfloadoptions/recognizeUtf8Text/
---

## RtfLoadOptions.recognizeUtf8Text property

When set to ``true``,  will try to detect UTF8 characters, 
they will be preserved during import.





```js
get recognizeUtf8Text(): boolean
```

### Remarks

Default value is ``false``.




### Examples

Shows how to detect UTF-8 characters while loading an RTF document.

```js
// Create an "RtfLoadOptions" object to modify how we load an RTF document.
let loadOptions = new aw.Loading.RtfLoadOptions();

// Set the "RecognizeUtf8Text" property to "false" to assume that the document uses the ISO 8859-1 charset
// and loads every character in the document.
// Set the "RecognizeUtf8Text" property to "true" to parse any variable-length characters that may occur in the text.
loadOptions.recognizeUtf8Text = recognizeUtf8Text;

let doc = new aw.Document(base.myDir + "UTF-8 characters.rtf", loadOptions);

expect(doc.firstSection.body.getText().trim()).toEqual(recognizeUtf8Text
  ? "“John Doe´s list of currency symbols”™\r€, ¢, £, ¥, ¤"
  : "â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\râ‚¬, Â¢, Â£, Â¥, Â¤");
```

### See Also

* module [Aspose.Words.Loading](../../)
* class [RtfLoadOptions](../)

