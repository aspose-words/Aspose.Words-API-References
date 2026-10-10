---
title: "Aspose::Words::Document::get_AutomaticallyUpdateStyles-metod"
linktitle: "get_AutomaticallyUpdateStyles"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::get_AutomaticallyUpdateStyles-metod. Hämtar eller anger en flagga som indikerar om stilarna i dokumentet uppdateras för att matcha stilarna i den bifogade mallen varje gång dokumentet öppnas i MS Word i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words/document/get_automaticallyupdatestyles/
---
## Document::get_AutomaticallyUpdateStyles method


Hämtar eller anger en flagga som indikerar om stilarna i dokumentet uppdateras för att matcha stilarna i den bifogade mallen varje gång dokumentet öppnas i MS Word.

```cpp
bool Aspose::Words::Document::get_AutomaticallyUpdateStyles()
```


## Exempel



Visar hur man bifogar en mall till ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Microsoft Word-dokument har som standard en bifogad mall som heter "Normal.dotm".
// Det finns ingen standardmall för tomma Aspose.Words-dokument.
ASSERT_EQ(System::String::Empty, doc->get_AttachedTemplate());

// Bifoga en mall, sätt sedan flaggan för att tillämpa stiländringar
// inom mallen på stilarna i vårt dokument.
doc->set_AttachedTemplate(get_MyDir() + u"Business brochure.dotx");
doc->set_AutomaticallyUpdateStyles(true);

doc->Save(get_ArtifactsDir() + u"Document.AutomaticallyUpdateStyles.docx");
```


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
