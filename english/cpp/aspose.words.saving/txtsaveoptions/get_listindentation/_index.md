---
title: get_ListIndentation
second_title: Aspose.Words for C++ API Reference
description: Gets a TxtListIndentation object that specifies how many and which character to use for indentation of list levels. By default it is zero count of character '\0', that means no indentation.
type: docs
weight: 40
url: /cpp/aspose.words.saving/txtsaveoptions/get_listindentation/
---
## TxtSaveOptions::get_ListIndentation method


Gets a [TxtListIndentation](../../txtlistindentation/) object that specifies how many and which character to use for indentation of list levels. By default it is zero count of character '\0', that means no indentation.

```cpp
System::SharedPtr<Aspose::Words::Saving::TxtListIndentation> Aspose::Words::Saving::TxtSaveOptions::get_ListIndentation() const
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

* Class [TxtListIndentation](../../txtlistindentation/)
* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
