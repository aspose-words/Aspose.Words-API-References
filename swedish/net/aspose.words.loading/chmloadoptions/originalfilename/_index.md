---
title: ChmLoadOptions.OriginalFileName
linktitle: OriginalFileName
articleTitle: OriginalFileName
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChmLoadOptions OriginalFileName, ställ enkelt in CHM-filnamnet för effektiv åtkomst. Standardvärdet är null. Optimera din upplevelse!
type: docs
weight: 20
url: /sv/net/aspose.words.loading/chmloadoptions/originalfilename/
---
## ChmLoadOptions.OriginalFileName property

Namnet på CHM-filen. Standardvärdet är`null` .

```csharp
public string OriginalFileName { get; set; }
```

## Anmärkningar

CHM-dokument kan innehålla länkar som refererar till samma dokument med filnamn. Aspose.Words stöder sådana länkar och använder normalt[`OriginalFileName`](../../../aspose.words/document/originalfilename/) för att kontrollera om filen som refereras av en länk är den fil som laddas. Om ett dokument laddas från en ström bör dess ursprungliga filnamn anges explicit via den här egenskapen, eftersom det inte kan bestämmas automatiskt.

Om ett CHM-dokument laddas från en fil och ett värde som inte är null anges för den här egenskapen, kommer värdet att prioriteras framför det faktiska namnet på filen som lagras i[`OriginalFileName`](../../../aspose.words/document/originalfilename/) .

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
