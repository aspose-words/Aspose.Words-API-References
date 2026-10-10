---
title: "Aspose::Words::Saving::SaveOptions::get_DefaultTemplate‑metod"
linktitle: "get_DefaultTemplate"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::SaveOptions::get_DefaultTemplate‑metod. Hämtar eller anger sökväg till standardmall (inklusive filnamn). Standardvärdet för denna egenskap är en tom sträng i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.saving/saveoptions/get_defaulttemplate/
---
## SaveOptions::get_DefaultTemplate method


Hämtar eller anger sökvägen till standardmall (inklusive filnamn). Standardvärdet för denna egenskap är **empty string**.

```cpp
System::String Aspose::Words::Saving::SaveOptions::get_DefaultTemplate() const
```


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

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
