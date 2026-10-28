---
title: Aspose::Words::Saving::TxtSaveOptions::set_SaveFormat method
linktitle: set_SaveFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::TxtSaveOptions::set_SaveFormat method. Specifies the format in which the document will be saved if this save options object is used. Can only be Text in C++.'
type: docs
weight: 14000
url: /cpp/aspose.words.saving/txtsaveoptions/set_saveformat/
---
## TxtSaveOptions::set_SaveFormat method


Specifies the format in which the document will be saved if this save options object is used. Can only be [Text](../../../aspose.words/saveformat/).

```cpp
void Aspose::Words::Saving::TxtSaveOptions::set_SaveFormat(Aspose::Words::SaveFormat value) override
```

## Examples


Shows how to save a .txt document with a custom paragraph break.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");
builder->Write(u"Paragraph 3.");

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
// to modify how we save the document to plaintext.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

ASSERT_EQ(SaveFormat::Text, txtSaveOptions->get_SaveFormat());

// Set the "ParagraphBreak" to a custom value that we wish to put at the end of every paragraph.
txtSaveOptions->set_ParagraphBreak(u" End of paragraph.\n\n\t");

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt");

ASSERT_EQ(System::String(u"Paragraph 1. End of paragraph.\n\n\t") + u"Paragraph 2. End of paragraph.\n\n\t" + u"Paragraph 3. End of paragraph.\n\n\t", docText);
```
## See Also

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
