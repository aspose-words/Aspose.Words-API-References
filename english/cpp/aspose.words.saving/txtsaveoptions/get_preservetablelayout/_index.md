---
title: get_PreserveTableLayout
second_title: Aspose.Words for C++ API Reference
description: Specifies whether the program should attempt to preserve layout of tables when saving in the plain text format. The default value is false.
type: docs
weight: 66
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

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
auto txtSaveOptions = MakeObject<TxtSaveOptions>();

// Set the "PreserveTableLayout" property to "true" to apply whitespace padding to the contents
// of the output plaintext document to preserve as much of the table's layout as possible.
// Set the "PreserveTableLayout" property to "false" to save all tables' contents
// as a continuous body of text, with just a new line for each row.
txtSaveOptions->set_PreserveTableLayout(preserveTableLayout);

doc->Save(ArtifactsDir + u"TxtSaveOptions.PreserveTableLayout.txt", txtSaveOptions);

String docText = System::IO::File::ReadAllText(ArtifactsDir + u"TxtSaveOptions.PreserveTableLayout.txt");

if (preserveTableLayout)
{
    ASSERT_EQ(String(u"Row 1, cell 1                                            Row 1, cell 2\r\n") +
                  u"Row 2, cell 1                                            Row 2, cell 2\r\n\r\n",
              docText);
}
else
{
    ASSERT_EQ(String(u"Row 1, cell 1\r") + u"Row 1, cell 2\r" + u"Row 2, cell 1\r" + u"Row 2, cell 2\r\r\n", docText);
}
```

## See Also

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
