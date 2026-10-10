---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary-metod"
linktitle: "get_IsTemporary"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary-metod. Anger om detta SDT ska tas bort från WordProcessingML-dokumentet när dess innehåll ändras i C++."
type: docs
weight: 19000
url: /sv/cpp/aspose.words.markup/structureddocumenttag/get_istemporary/
---
## StructuredDocumentTag::get_IsTemporary method


Anger om detta **SDT** ska tas bort från WordProcessingML‑dokumentet när dess innehåll ändras.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary() const
```


## Exempel



Visar hur man skapar engångskontroller.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Infoga en strukturerad dokumenttagg med vanlig text,
// som fungerar som ett vanligt textformulär som användaren kan skriva in text i.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Ställ in egenskapen "IsTemporary" till "true" för att få den strukturerade dokumenttaggen att försvinna och
// absorbera dess innehåll i dokumentet efter att användaren har redigerat den en gång i Microsoft Word.
// Ställ in egenskapen "IsTemporary" till "false" för att tillåta användaren att redigera innehållet
// i den strukturerade dokumenttaggen hur många gånger som helst.
tag->set_IsTemporary(isTemporary);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Please enter text: ");
builder->InsertNode(tag);

// Infoga en annan strukturerad dokumenttagg i form av en kryssruta och ställ in dess standardläge till "checked".
tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Checkbox, Aspose::Words::Markup::MarkupLevel::Inline);
tag->set_Checked(true);

// Ställ in egenskapen "IsTemporary" till "true" för att få kryssrutan att bli en symbol
// när användaren klickar på den i Microsoft Word.
// Ställ in egenskapen "IsTemporary" till "false" för att tillåta användaren att klicka på kryssrutan hur många gånger som helst.
tag->set_IsTemporary(isTemporary);

builder->Write(u"\nPlease click the check box: ");
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.IsTemporary.docx");
```

## Se även

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
