---
title: "Aspose::Words::Saving::SaveOptions::CreateSaveOptions metod"
linktitle: "CreateSaveOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::SaveOptions::CreateSaveOptions metod. Skapar ett spara‑alternativ‑objekt av en klass som är lämplig för det angivna sparformatet i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.saving/saveoptions/createsaveoptions/
---
## SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat) method


Skapar ett spara‑alternativ‑objekt av en klass som är lämplig för det angivna spara‑formatet.

```cpp
static System::SharedPtr<Aspose::Words::Saving::SaveOptions> Aspose::Words::Saving::SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Sparformatet för vilket ett spara‑alternativ‑objekt ska skapas. |

### ReturnValue

Ett objekt av en klass som ärver från [SaveOptions](../).

## Se även

* Class [SaveOptions](../)
* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## SaveOptions::CreateSaveOptions(const System::String\&) method


Skapar ett sparaalternativobjekt av en klass som är lämplig för filändelsen som anges i det givna filnamnet.

```cpp
static System::SharedPtr<Aspose::Words::Saving::SaveOptions> Aspose::Words::Saving::SaveOptions::CreateSaveOptions(const System::String &fileName)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | const System::String\& | Filnamnstillägget bestämmer vilken klass av spara‑alternativ‑objekt som ska skapas. |

### ReturnValue

Ett objekt av en klass som ärver från [SaveOptions](../).

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
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
