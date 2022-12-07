---
title: get_IsPathRelative
second_title: Aspose.Words for C++ API Reference
description: Gets or sets whether the path is relative to the current document.
type: docs
weight: 27
url: /cpp/aspose.words.fields/fieldrd/get_ispathrelative/
---
## FieldRD::get_IsPathRelative method


Gets or sets whether the path is relative to the current document.

```cpp
bool Aspose::Words::Fields::FieldRD::get_IsPathRelative()
```


## Examples



Shows to use the RD field to create a table of contents entries from headings in other documents. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Use a document builder to insert a table of contents,
// and then add one entry for the table of contents on the following page.
builder->InsertField(FieldType::FieldTOC, true);
builder->InsertBreak(BreakType::PageBreak);
builder->get_CurrentParagraph()->get_ParagraphFormat()->set_StyleName(u"Heading 1");
builder->Writeln(u"TOC entry from within this document");

// Insert an RD field, which references another local file system document in its FileName property.
// The TOC will also now accept all headings from the referenced document as entries for its table.
auto field = System::DynamicCast<FieldRD>(builder->InsertField(FieldType::FieldRefDoc, true));
field->set_FileName(u"ReferencedDocument.docx");
field->set_IsPathRelative(true);

ASSERT_EQ(u" RD  ReferencedDocument.docx \\f", field->GetFieldCode());

// Create the document that the RD field is referencing and insert a heading.
// This heading will show up as an entry in the TOC field in our first document.
auto referencedDoc = MakeObject<Document>();
auto refDocBuilder = MakeObject<DocumentBuilder>(referencedDoc);
refDocBuilder->get_CurrentParagraph()->get_ParagraphFormat()->set_StyleName(u"Heading 1");
refDocBuilder->Writeln(u"TOC entry from referenced document");
referencedDoc->Save(ArtifactsDir + u"ReferencedDocument.docx");

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.RD.docx");
```

## See Also

* Class [FieldRD](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
