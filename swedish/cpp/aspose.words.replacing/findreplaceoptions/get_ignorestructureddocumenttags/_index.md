---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags method"
linktitle: "get_IgnoreStructuredDocumentTags"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags method. Hämtar eller anger ett booleskt värde som indikerar om innehållet i StructuredDocumentTag ska ignoreras. Standardvärdet är false i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words.replacing/findreplaceoptions/get_ignorestructureddocumenttags/
---
## FindReplaceOptions::get_IgnoreStructuredDocumentTags method


Hämtar eller anger ett booleskt värde som indikerar om innehållet i [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) ska ignoreras. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags() const
```

## Anmärkningar


När detta alternativ är satt till **true** kommer innehållet i [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) att behandlas som enkel text.

Annars kommer [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) att behandlas som en fristående [Story](../../../aspose.words/story/) och ersättningsmönstret kommer att sökas separat för varje [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), så att om mönstret korsar ett [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) så kommer ersättningen inte att utföras för ett sådant mönster.

## Exempel



Visar hur man ignorerar innehållet i taggar vid ersättning.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// Detta stycke innehåller SDT.
auto p = System::ExplicitCast<Aspose::Words::Paragraph>(doc->get_FirstSection()->get_Body()->GetChild(Aspose::Words::NodeType::Paragraph, 2, true));
System::String textToSearch = p->ToString(Aspose::Words::SaveFormat::Text).Trim();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreStructuredDocumentTags(true);
doc->get_Range()->Replace(textToSearch, u"replacement", options);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
```

## Se även

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
