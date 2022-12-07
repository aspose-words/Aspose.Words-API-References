---
title: get_ParagraphBreak
second_title: Aspose.Words for C++ API Reference
description: Specifies the string to use as a paragraph break when exporting in text formats.
type: docs
weight: 66
url: /cpp/aspose.words.saving/txtsaveoptionsbase/get_paragraphbreak/
---
## TxtSaveOptionsBase::get_ParagraphBreak method


Specifies the string to use as a paragraph break when exporting in text formats.

```cpp
System::String Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak() const
```

## Remarks


The default value is [CrLf](../../../aspose.words/controlchar/crlf/).

## Examples



Shows how to save a .txt document with a custom paragraph break. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");
builder->Write(u"Paragraph 3.");

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
// to modify how we save the document to plaintext.
auto txtSaveOptions = MakeObject<TxtSaveOptions>();

ASSERT_EQ(SaveFormat::Text, txtSaveOptions->get_SaveFormat());

// Set the "ParagraphBreak" to a custom value that we wish to put at the end of every paragraph.
txtSaveOptions->set_ParagraphBreak(u" End of paragraph.\n\n\t");

doc->Save(ArtifactsDir + u"TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

String docText = System::IO::File::ReadAllText(ArtifactsDir + u"TxtSaveOptions.ParagraphBreak.txt");

ASSERT_EQ(String(u"Paragraph 1. End of paragraph.\n\n\t") + u"Paragraph 2. End of paragraph.\n\n\t" + u"Paragraph 3. End of paragraph.\n\n\t", docText);
```

## See Also

* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
