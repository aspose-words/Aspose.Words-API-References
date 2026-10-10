---
title: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri metod"
linktitle: "get_ResourceFileUri"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri metod. Hämtar eller anger den enhetliga resursidentifieraren (URI) som används för att referera till resursfilen från dokumentet i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.saving/resourcesavingargs/get_resourcefileuri/
---
## ResourceSavingArgs::get_ResourceFileUri method


Hämtar eller anger den uniforma resursidentifieraren (URI) som används för att referera till resursfilen från dokumentet.

```cpp
System::String Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri() const
```

## Anmärkningar


Denna egenskap låter dig ändra URI:er för resursfiler som exporteras till fasta HTML‑sidor, SVG‑ eller Markdown‑dokument.

Aspose.Words genererar automatiskt en URI för varje resursfil vid export till fast HTML‑sida, SVG‑ eller Markdown‑format. De genererade URI:erna refererar till resursfiler som sparats av Aspose.Words. Däremot kan URI:erna vara felaktiga om resursfiler ska flyttas till en annan plats eller om resursfiler sparas till strömmar. Denna egenskap gör det möjligt att korrigera URI:erna i dessa fall.

När händelsen utlöses innehåller denna egenskap den URI som genererades av Aspose.Words. Du kan ändra värdet på denna egenskap för att ange en anpassad URI för resursfilen.
## Se även

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
