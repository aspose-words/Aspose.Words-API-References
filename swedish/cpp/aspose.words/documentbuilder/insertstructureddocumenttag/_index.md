---
title: "Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag metod"
linktitle: "InsertStructuredDocumentTag"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag metod. Infogar en StructuredDocumentTag i dokumentet i C++."
type: docs
weight: 46500
url: /sv/cpp/aspose.words/documentbuilder/insertstructureddocumenttag/
---
## DocumentBuilder::InsertStructuredDocumentTag method


Infogar en [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) i dokumentet.

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag(Aspose::Words::Markup::SdtType type)
```


### ReturnValue

Den [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) nod som just infogades.

## Exempel



Visar hur man enkelt infogar en strukturerad dokumenttagg.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveTo(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(3));
// Observera att endast följande StructuredDocumentTag-typer är tillåtna för infogning:
// SdtType.PlainText, SdtType.RichText, SdtType.Checkbox, SdtType.DropDownList,
// SdtType.ComboBox, SdtType.Picture, SdtType.Date.
// Markup-nivån för den infogade StructuredDocumentTag kommer att upptäckas automatiskt och beror på den position där den infogas.
// Tillagd StructuredDocumentTag kommer att ärva stycke- och teckensnittsformatering från markörens position.
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> sdtPlain = builder->InsertStructuredDocumentTag(Aspose::Words::Markup::SdtType::PlainText);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.InsertStructuredDocumentTag.docx");
```

## Se även

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Enum [SdtType](../../../aspose.words.markup/sdttype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
