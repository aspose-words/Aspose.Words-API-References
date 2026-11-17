---
title: Aspose::Words::Saving::TxtListIndentation::get_Count method
linktitle: get_Count
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::TxtListIndentation::get_Count method. Gets or sets how many Character to use as indentation per one list level. The default value is 0, that means no indentation in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.saving/txtlistindentation/get_count/
---
## TxtListIndentation::get_Count method


Gets or sets how many [Character](../get_character/) to use as indentation per one list level. The default value is 0, that means no indentation.

```cpp
int32_t Aspose::Words::Saving::TxtListIndentation::get_Count() const
```


## Examples



Shows how to configure list indenting when saving a document to plaintext. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Create a list with three levels of indentation.
builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Item 1");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 2");
builder->get_ListFormat()->ListIndent();
builder->Write(u"Item 3");

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
// to modify how we save the document to plaintext.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Set the "Character" property to assign a character to use
// for padding that simulates list indentation in plaintext.
txtSaveOptions->get_ListIndentation()->set_Character(u' ');

// Set the "Count" property to specify the number of times
// to place the padding character for each list indent level.
txtSaveOptions->get_ListIndentation()->set_Count(3);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt");
System::String newLine = System::Environment::get_NewLine();

ASSERT_EQ(System::String::Format(u"1. Item 1{0}", newLine) + System::String::Format(u"   a. Item 2{0}", newLine) + System::String::Format(u"      i. Item 3{0}", newLine), docText);
```

## See Also

* Class [TxtListIndentation](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
