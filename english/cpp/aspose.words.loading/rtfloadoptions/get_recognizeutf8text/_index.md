---
title: Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text method
linktitle: get_RecognizeUtf8Text
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text method. When set to true, will try to detect UTF8 characters, they will be preserved during import in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.loading/rtfloadoptions/get_recognizeutf8text/
---
## RtfLoadOptions::get_RecognizeUtf8Text method


When set to **true**, will try to detect UTF8 characters, they will be preserved during import.

```cpp
bool Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text() const
```

## Remarks


Default value is **false**.

## Examples



Shows how to detect UTF-8 characters while loading an RTF document. 
```cpp
// Create an "RtfLoadOptions" object to modify how we load an RTF document.
auto loadOptions = MakeObject<RtfLoadOptions>();

// Set the "RecognizeUtf8Text" property to "false" to assume that the document uses the ISO 8859-1 charset
// and loads every character in the document.
// Set the "RecognizeUtf8Text" property to "true" to parse any variable-length characters that may occur in the text.
loadOptions->set_RecognizeUtf8Text(recognizeUtf8Text);

auto doc = MakeObject<Document>(MyDir + u"UTF-8 characters.rtf", loadOptions);

ASSERT_EQ(recognizeUtf8Text ? String(u"“John Doe´s list of currency symbols”™\r") + u"€, ¢, £, ¥, ¤"
                            : String(u"â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r") + u"â‚¬, Â¢, Â£, Â¥, Â¤",
          doc->get_FirstSection()->get_Body()->GetText().Trim());
```

## See Also

* Class [RtfLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
