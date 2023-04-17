---
title: Aspose::Words::Saving::TxtListIndentation::get_Character method
linktitle: get_Character
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::TxtListIndentation::get_Character method. Gets or sets which character to use for indenting list levels. The default value is ''\0'', that means there is no indentation in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.saving/txtlistindentation/get_character/
---
## TxtListIndentation::get_Character method


Gets or sets which character to use for indenting list levels. The default value is '\0', that means there is no indentation.

```cpp
char16_t Aspose::Words::Saving::TxtListIndentation::get_Character() const
```


## Examples



Shows how to configure list indenting when saving a document to plaintext. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Create a list with three levels of indentation.
builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Item 1");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 2");
builder->get_ListFormat()->ListIndent();
builder->Write(u"Item 3");

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
// to modify how we save the document to plaintext.
auto txtSaveOptions = MakeObject<TxtSaveOptions>();

// Set the "Character" property to assign a character to use
// for padding that simulates list indentation in plaintext.
txtSaveOptions->get_ListIndentation()->set_Character(u' ');

// Set the "Count" property to specify the number of times
// to place the padding character for each list indent level.
txtSaveOptions->get_ListIndentation()->set_Count(3);

doc->Save(ArtifactsDir + u"TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

String docText = System::IO::File::ReadAllText(ArtifactsDir + u"TxtSaveOptions.TxtListIndentation.txt");

ASSERT_EQ(String(u"1. Item 1\r\n") + u"   a. Item 2\r\n" + u"      i. Item 3\r\n", docText);
```

## See Also

* Class [TxtListIndentation](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
