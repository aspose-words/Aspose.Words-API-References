---
title: "Aspose::Words::Loading::LoadOptions::get_TempFolder metod"
linktitle: "get_TempFolder"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::LoadOptions::get_TempFolder metod. Tillåter att använda temporära filer vid läsning av dokument. Som standard är denna egenskap null och inga temporära filer används i C++."
type: docs
weight: 16000
url: /sv/cpp/aspose.words.loading/loadoptions/get_tempfolder/
---
## LoadOptions::get_TempFolder method


Tillåter att använda temporära filer när dokument läses. Som standard är denna egenskap **null** och inga temporära filer används.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_TempFolder() const
```

## Anmärkningar


Mappen måste finnas och vara skrivbar, annars kommer ett undantag att kastas.

Aspose.Words tar automatiskt bort alla temporära filer när läsningen är klar.

## Exempel



Visar hur man läser in ett dokument med hjälp av temporära filer.
```cpp
// Observera att en sådan metod kan minska minnesanvändningen men försämrar hastigheten.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_TempFolder(u"C:\\TempFolder\\");

// Säkerställ att katalogen finns och läs in.
System::IO::Directory::CreateDirectory_(loadOptions->get_TempFolder());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);
```


Visar hur man använder hårddisken istället för minnet när ett dokument läses in.
```cpp
// När vi läser in ett dokument lagras olika element tillfälligt i minnet när sparningsoperationen sker.
// Vi kan använda detta alternativ för att istället använda en temporär mapp i det lokala filsystemet,
// vilket kommer att minska vår applikations minnesbelastning.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
options->set_TempFolder(get_ArtifactsDir() + u"TempFiles");

// Den angivna temporära mappen måste finnas i det lokala filsystemet innan inläsningsoperationen.
System::IO::Directory::CreateDirectory_(options->get_TempFolder());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", options);

// Mappen kommer att bestå utan några återstående innehåll från laddningsoperationen.
ASSERT_EQ(0, System::IO::Directory::GetFiles(options->get_TempFolder())->get_Length());
```

## Se även

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
