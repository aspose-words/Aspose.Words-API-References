---
title: Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks method
linktitle: get_AddBidiMarks
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks method. Specifies whether to add bi-directional marks before each BiDi run when exporting in plain text format. The default value is false in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.saving/txtsaveoptions/get_addbidimarks/
---
## TxtSaveOptions::get_AddBidiMarks method


Specifies whether to add bi-directional marks before each BiDi run when exporting in plain text format. The default value is **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks() const
```


## Examples



Shows how to insert Unicode Character 'RIGHT-TO-LEFT MARK' (U+200F) before each bi-directional [Run](../../../aspose.words/run/) in text. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->get_ParagraphFormat()->set_Bidi(true);
builder->Writeln(u"שלום עולם!");
builder->Writeln(u"مرحبا بالعالم!");

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
// to modify how we save the document to plaintext.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_Encoding(System::Text::Encoding::get_Unicode());

// Set the "AddBidiMarks" property to "true" to add marks before runs
// with right-to-left text to indicate the fact.
// Set the "AddBidiMarks" property to "false" to write all left-to-right
// and right-to-left run equally with nothing to indicate which is which.
saveOptions->set_AddBidiMarks(addBidiMarks);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.AddBidiMarks.txt", saveOptions);

System::String docText = System::Text::Encoding::get_Unicode()->GetString(System::IO::File::ReadAllBytes(get_ArtifactsDir() + u"TxtSaveOptions.AddBidiMarks.txt"));

if (addBidiMarks)
{
    ASSERT_EQ(u"\ufeffHello world!‎\r\nשלום עולם!‏\r\nمرحبا بالعالم!‏\r\n\r\n", docText);
    ASSERT_TRUE(docText.Contains(u"\u200f"));
}
else
{
    ASSERT_EQ(u"\ufeffHello world!\r\nשלום עולם!\r\nمرحبا بالعالم!\r\n\r\n", docText);
    ASSERT_FALSE(docText.Contains(u"\u200f"));
}
```

## See Also

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
