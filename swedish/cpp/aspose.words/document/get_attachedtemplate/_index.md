---
title: "Aspose::Words::Document::get_AttachedTemplate metod"
linktitle: "get_AttachedTemplate"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::get_AttachedTemplate metod. Hämtar eller anger den fullständiga sökvägen till mallen som är kopplad till dokumentet i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words/document/get_attachedtemplate/
---
## Document::get_AttachedTemplate method


Hämtar eller anger den fullständiga sökvägen till mallen som är bifogad dokumentet.

```cpp
System::String Aspose::Words::Document::get_AttachedTemplate()
```

## Anmärkningar


Tom sträng betyder att dokumentet är kopplat till Normal-mallen.

## Exempel



Visar hur man anger en standardmall för dokument som inte har bifogade mallar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Aktivera automatisk stiluppdatering, men bifoga inte ett mall-dokument.
doc->set_AutomaticallyUpdateStyles(true);

ASSERT_EQ(System::String::Empty, doc->get_AttachedTemplate());

// Eftersom det inte finns något mall-dokument, hade dokumentet ingen plats att spåra stiländringar.
// Använd ett SaveOptions-objekt för att automatiskt ange en mall
// om ett dokument som vi sparar inte har en.
System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = Aspose::Words::Saving::SaveOptions::CreateSaveOptions(u"Document.DefaultTemplate.docx");
options->set_DefaultTemplate(get_MyDir() + u"Business brochure.dotx");

doc->Save(get_ArtifactsDir() + u"Document.DefaultTemplate.docx", options);
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
