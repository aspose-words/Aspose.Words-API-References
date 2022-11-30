---
title: get_IgnoreTextBoxes
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a boolean value that specifies that source formatting of textboxes content ignored if KeepSourceFormatting mode is used. The default value is true.
type: docs
weight: 40
url: /cpp/aspose.words/importformatoptions/get_ignoretextboxes/
---
## ImportFormatOptions::get_IgnoreTextBoxes method


Gets or sets a boolean value that specifies that source formatting of textboxes content ignored if [KeepSourceFormatting](../../importformatmode/) mode is used. The default value is **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes() const
```


## Examples



Shows how to manage text box formatting while appending a document. 
```cpp
// Create a document that will have nodes from another document inserted into it.
auto dstDoc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(dstDoc);

builder->Writeln(u"Hello world!");

// Create another document with a text box, which we will import into the first document.
auto srcDoc = MakeObject<Document>();
builder = MakeObject<DocumentBuilder>(srcDoc);

SharedPtr<Shape> textBox = builder->InsertShape(ShapeType::TextBox, 300, 100);
builder->MoveTo(textBox->get_FirstParagraph());
builder->get_ParagraphFormat()->get_Style()->get_Font()->set_Name(u"Courier New");
builder->get_ParagraphFormat()->get_Style()->get_Font()->set_Size(24);
builder->Write(u"Textbox contents");

// Set a flag to specify whether to clear or preserve text box formatting
// while importing them to other documents.
auto importFormatOptions = MakeObject<ImportFormatOptions>();
importFormatOptions->set_IgnoreTextBoxes(ignoreTextBoxes);

// Import the text box from the source document into the destination document,
// and then verify whether we have preserved the styling of its text contents.
auto importer = MakeObject<NodeImporter>(srcDoc, dstDoc, ImportFormatMode::KeepSourceFormatting, importFormatOptions);
auto importedTextBox = System::DynamicCast<Shape>(importer->ImportNode(textBox, true));
dstDoc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->AppendChild(importedTextBox);

if (ignoreTextBoxes)
{
    ASPOSE_ASSERT_EQ(12.0, importedTextBox->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Size());
    ASSERT_EQ(u"Times New Roman", importedTextBox->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());
}
else
{
    ASPOSE_ASSERT_EQ(24.0, importedTextBox->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Size());
    ASSERT_EQ(u"Courier New", importedTextBox->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());
}

dstDoc->Save(ArtifactsDir + u"DocumentBuilder.IgnoreTextBoxes.docx");
```

## See Also

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
