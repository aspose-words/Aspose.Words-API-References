---
title: ChmLoadOptions.OriginalFileName
linktitle: OriginalFileName
articleTitle: OriginalFileName
second_title: Aspose.Words för .NET
description: ChmLoadOptions OriginalFileName fast egendom. Namnet på CHMfilen. Standardvärdet ärnull  i C#.
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

CHM-dokument kan innehålla länkar som refererar till samma dokument efter filnamn. Aspose.Words stöder sådana links och använder normalt[`OriginalFileName`](../../../aspose.words/document/originalfilename/) för att kontrollera om filen som refereras till av en link är den fil som laddas. Om ett dokument laddas från en ström, bör dess ursprungliga filnamn specificeras uttryckligen via den här egenskapen, eftersom det inte kan fastställas automatiskt.

Om ett CHM-dokument laddas från en fil och ett icke-nullvärde för den här egenskapen anges, kommer värdet att ta prioritet över det faktiska namnet på filen som lagras i[`OriginalFileName`](../../../aspose.words/document/originalfilename/) .

## Exempel

Visar hur man löser webbadresser som "ms-its:myfile.chm::/index.htm".

```csharp
// Vårt dokument innehåller webbadresser som "ms-its:amhelp.chm::....htm", men det har ett annat namn,
// så fillänkar fungerar inte efter att ha sparats i HTML.
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
