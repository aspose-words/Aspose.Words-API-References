---
title: get_SaveFormat
second_title: Aspose.Words for C++ API Reference
description: Specifies the format in which the document will be saved if this save options object is used. Can only be Text.
type: docs
weight: 66
url: /cpp/aspose.words.saving/txtsaveoptions/get_saveformat/
---
## TxtSaveOptions.get_SaveFormat method


Specifies the format in which the document will be saved if this save options object is used. Can only be **Text**.

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::TxtSaveOptions::get_SaveFormat() override
```


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

