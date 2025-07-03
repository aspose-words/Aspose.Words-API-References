---
title: Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag method
linktitle: InsertStructuredDocumentTag
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag method. Inserts a StructuredDocumentTag into the document in C++.'
type: docs
weight: 46500
url: /cpp/aspose.words/documentbuilder/insertstructureddocumenttag/
---
## DocumentBuilder::InsertStructuredDocumentTag method


Inserts a [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) into the document.

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag(Aspose::Words::Markup::SdtType type)
```


### ReturnValue

The [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) node that was just inserted.

## Examples



Shows how to simply insert structured document tag. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveTo(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(3));
// Note, that only following StructuredDocumentTag types are allowed for insertion:
// SdtType.PlainText, SdtType.RichText, SdtType.Checkbox, SdtType.DropDownList,
// SdtType.ComboBox, SdtType.Picture, SdtType.Date.
// Markup level of inserted StructuredDocumentTag will be detected automatically and depends on position being inserted at.
// Added StructuredDocumentTag will inherit paragraph and font formatting from cursor position.
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> sdtPlain = builder->InsertStructuredDocumentTag(Aspose::Words::Markup::SdtType::PlainText);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.InsertStructuredDocumentTag.docx");
```

## See Also

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Enum [SdtType](../../../aspose.words.markup/sdttype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
