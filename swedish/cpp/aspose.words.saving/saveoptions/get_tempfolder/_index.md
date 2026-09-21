---
title: "Aspose::Words::Saving::SaveOptions::get_TempFolder‑metod"
linktitle: "get_TempFolder"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::SaveOptions::get_TempFolder‑metod. Anger mappen för temporära filer som används vid sparande till en DOC‑ eller DOCX‑fil. Som standard är denna egenskap null och inga temporära filer används i C++."
type: docs
weight: 15000
url: /sv/cpp/aspose.words.saving/saveoptions/get_tempfolder/
---
## SaveOptions::get_TempFolder method


Anger mappen för temporära filer som används vid sparande till en DOC- eller DOCX-fil. Som standard är denna egenskap **null** och inga temporära filer används.

```cpp
System::String Aspose::Words::Saving::SaveOptions::get_TempFolder() const
```

## Anmärkningar


När Aspose.Words sparar ett dokument måste det skapa temporära interna strukturer. Som standard skapas dessa interna strukturer i minnet och minnesanvändningen ökar kraftigt under en kort period medan dokumentet sparas. När sparandet är klart frigörs minnet och återtas av skräpsamlaren.

Om du anger en temporär mapp med hjälp av [TempFolder](./) kommer Aspose.Words att lagra de interna strukturerna i temporära filer istället för i minnet. Det minskar minnesanvändningen under sparandet, men sänker sparprestandan.

Mappen måste finnas och vara skrivbar, annars kommer ett undantag att kastas.

Aspose.Words tar automatiskt bort alla temporära filer när sparandet är slutfört.

## Exempel



Visar hur man använder hårddisken istället för minnet när ett dokument sparas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// När vi sparar ett dokument lagras olika element tillfälligt i minnet medan sparoperationen pågår.
// Vi kan använda detta alternativ för att istället använda en temporär mapp i det lokala filsystemet,
// vilket kommer att minska vår applikations minnesbelastning.
auto options = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
options->set_TempFolder(get_ArtifactsDir() + u"TempFiles");

// Den angivna temporära mappen måste finnas i det lokala filsystemet innan sparoperationen.
System::IO::Directory::CreateDirectory_(options->get_TempFolder());

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.TempFolder.doc", options);

// Mappen kommer att bestå utan några återstående innehåll från laddningsoperationen.
ASSERT_EQ(0, System::IO::Directory::GetFiles(options->get_TempFolder())->get_Length());
```

## Se även

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
