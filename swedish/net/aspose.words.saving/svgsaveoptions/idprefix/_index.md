---
title: SvgSaveOptions.IdPrefix
linktitle: IdPrefix
articleTitle: IdPrefix
second_title: Aspose.Words för .NET
description: Upptäck egenskapen SvgSaveOptions IdPrefix, som anpassar element-ID:n i ditt utdatadokument för bättre organisation och tydlighet. Förbättra dina SVG-filer idag!
type: docs
weight: 40
url: /sv/net/aspose.words.saving/svgsaveoptions/idprefix/
---
## SvgSaveOptions.IdPrefix property

Anger ett prefix som läggs till före alla genererade element-ID:n i utdatadokumentet. Standardvärdet är null och inget prefix läggs till.

```csharp
public string IdPrefix { get; set; }
```

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentException | Värdet uppfyller inte kraven som anges ovan. |

## Anmärkningar

Om prefixet anges kan det endast innehålla bokstäver, siffror, understreck och bindestreck, och måste börja med en bokstav.

## Exempel

Visar hur man lägger till ett prefix som läggs till före alla genererade element-ID:n (svg).

```csharp
Document doc = new Document(MyDir + "Id prefix.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.IdPrefix = "pfx1_";

doc.Save(ArtifactsDir + "SvgSaveOptions.IdPrefixSvg.html", saveOptions);
```

### Se även

* class [SvgSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
