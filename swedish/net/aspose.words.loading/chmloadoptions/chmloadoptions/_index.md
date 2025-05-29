---
title: ChmLoadOptions
linktitle: ChmLoadOptions
articleTitle: ChmLoadOptions
second_title: Aspose.Words för .NET
description: Upptäck ChmLoadOptions-konstruktorn för sömlös initialisering. Ställ in standardvärden enkelt och förbättra din applikations prestanda idag!
type: docs
weight: 10
url: /sv/net/aspose.words.loading/chmloadoptions/chmloadoptions/
---
## ChmLoadOptions constructor

Initierar en ny instans av den här klassen med standardvärden.

```csharp
public ChmLoadOptions()
```

## Exempel

Visar hur man matchar URL:er som "ms-its:myfile.chm::/index.htm".

```csharp
// Vårt dokument innehåller webbadresser som "ms-its:amhelp.chm::....htm", men det har ett annat namn,
// så fillänkar fungerar inte efter att de har sparats i HTML.
// Vi måste definiera det ursprungliga filnamnet i 'ChmLoadOptions' för att undvika detta beteende.
ChmLoadOptions loadOptions = new ChmLoadOptions { OriginalFileName = "amhelp.chm" };

Document doc = new Document(new MemoryStream(File.ReadAllBytes(MyDir + "Document with ms-its links.chm")),
    loadOptions);

doc.Save(ArtifactsDir + "ExChmLoadOptions.OriginalFileName.html");
```

### Se även

* class [ChmLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
