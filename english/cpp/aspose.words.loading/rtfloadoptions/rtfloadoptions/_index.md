---
title: Aspose::Words::Loading::RtfLoadOptions::RtfLoadOptions constructor
linktitle: RtfLoadOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::RtfLoadOptions::RtfLoadOptions constructor. Initializes a new instance of this class with default values in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.loading/rtfloadoptions/rtfloadoptions/
---
## RtfLoadOptions::RtfLoadOptions constructor


Initializes a new instance of this class with default values.

```cpp
Aspose::Words::Loading::RtfLoadOptions::RtfLoadOptions()
```


## Examples



Shows how to detect UTF-8 characters while loading an RTF document. 
```cpp
// Create an "RtfLoadOptions" object to modify how we load an RTF document.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::RtfLoadOptions>();

// Set the "RecognizeUtf8Text" property to "false" to assume that the document uses the ISO 8859-1 charset
// and loads every character in the document.
// Set the "RecognizeUtf8Text" property to "true" to parse any variable-length characters that may occur in the text.
loadOptions->set_RecognizeUtf8Text(recognizeUtf8Text);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"UTF-8 characters.rtf", loadOptions);

ASSERT_EQ(recognizeUtf8Text ? System::String(u"“John Doe´s list of currency symbols”™\r") + u"€, ¢, £, ¥, ¤" : System::String(u"â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r") + u"â‚¬, Â¢, Â£, Â¥, Â¤", doc->get_FirstSection()->get_Body()->GetText().Trim());
```

## See Also

* Class [RtfLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
