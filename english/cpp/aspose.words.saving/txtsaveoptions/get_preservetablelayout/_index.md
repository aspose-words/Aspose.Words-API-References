---
title: Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout method
linktitle: get_PreserveTableLayout
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout method. Specifies whether the program should attempt to preserve layout of tables when saving in the plain text format. The default value is false in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.saving/txtsaveoptions/get_preservetablelayout/
---
## TxtSaveOptions::get_PreserveTableLayout method


Specifies whether the program should attempt to preserve layout of tables when saving in the plain text format. The default value is **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout() const
```


## Examples



Shows how to preserve the layout of tables when converting to plaintext. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1");
builder->InsertCell();
builder->Write(u"Row 1, cell 2");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, cell 1");
builder->InsertCell();
builder->Write(u"Row 2, cell 2");
builder->EndTable();

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
// to modify how we save the document to plaintext.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Set the "PreserveTableLayout" property to "true" to apply whitespace padding to the contents
// of the output plaintext document to preserve as much of the table's layout as possible.
// Set the "PreserveTableLayout" property to "false" to save all tables' contents
// as a continuous body of text, with just a new line for each row.
txtSaveOptions->set_PreserveTableLayout(preserveTableLayout);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.PreserveTableLayout.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.PreserveTableLayout.txt");

if (preserveTableLayout)
{
    ASSERT_EQ(System::String(u"Row 1, cell 1                                            Row 1, cell 2\r\n") + u"Row 2, cell 1                                            Row 2, cell 2\r\n\r\n", docText);
}
else
{
    ASSERT_EQ(System::String(u"Row 1, cell 1\r") + u"Row 1, cell 2\r" + u"Row 2, cell 1\r" + u"Row 2, cell 2\r\r\n", docText);
}
```

## See Also

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
