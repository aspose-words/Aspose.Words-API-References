---
title: get_Bidi
second_title: Aspose.Words for C++ API Reference
description: Gets or sets whether this is a right-to-left paragraph.
type: docs
weight: 66
url: /cpp/aspose.words/paragraphformat/get_bidi/
---
## ParagraphFormat::get_Bidi method


Gets or sets whether this is a right-to-left paragraph.

```cpp
bool Aspose::Words::ParagraphFormat::get_Bidi()
```

## Remarks


When **true**, the runs and other inline objects in this paragraph are laid out right to left.

## Examples



Shows how to create right-to-left language-compatible lists with BIDIOUTLINE fields. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// The BIDIOUTLINE field numbers paragraphs like the AUTONUM/LISTNUM fields,
// but is only visible when a right-to-left editing language is enabled, such as Hebrew or Arabic.
// The following field will display ".1", the RTL equivalent of list number "1.".
auto field = System::DynamicCast<FieldBidiOutline>(builder->InsertField(FieldType::FieldBidiOutline, true));
builder->Writeln(u"שלום");

ASSERT_EQ(u" BIDIOUTLINE ", field->GetFieldCode());

// Add two more BIDIOUTLINE fields, which will display ".2" and ".3".
builder->InsertField(FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");
builder->InsertField(FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");

// Set the horizontal text alignment for every paragraph in the document to RTL.
for (const auto& para : System::IterateOver<Paragraph>(doc->GetChildNodes(NodeType::Paragraph, true)))
{
    para->get_ParagraphFormat()->set_Bidi(true);
}

// If we enable a right-to-left editing language in Microsoft Word, our fields will display numbers.
// Otherwise, they will display "###".
doc->Save(ArtifactsDir + u"Field.BIDIOUTLINE.docx");
```


Shows how to detect plaintext document text direction. 
```cpp
// Create a "TxtLoadOptions" object, which we can pass to a document's constructor
// to modify how we load a plaintext document.
auto loadOptions = MakeObject<TxtLoadOptions>();

// Set the "DocumentDirection" property to "DocumentDirection.Auto" automatically detects
// the direction of every paragraph of text that Aspose.Words loads from plaintext.
// Each paragraph's "Bidi" property will store its direction.
loadOptions->set_DocumentDirection(DocumentDirection::Auto);

// Detect Hebrew text as right-to-left.
auto doc = MakeObject<Document>(MyDir + u"Hebrew text.txt", loadOptions);

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());

// Detect English text as right-to-left.
doc = MakeObject<Document>(MyDir + u"English text.txt", loadOptions);

ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());
```

## See Also

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
