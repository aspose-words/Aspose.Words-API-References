---
title: HtmlFixedSaveOptions.IdPrefix
linktitle: IdPrefix
articleTitle: IdPrefix
second_title: Aspose.Words för .NET
description: Upptäck egenskapen HtmlFixedSaveOptions IdPrefix för att anpassa element-ID:n i dina dokument. Förbättra organiseringen med skräddarsydda prefix för bättre resultat!
type: docs
weight: 100
url: /sv/net/aspose.words.saving/htmlfixedsaveoptions/idprefix/
---
## HtmlFixedSaveOptions.IdPrefix property

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

Visar hur man lägger till ett prefix som läggs till före alla genererade element-ID:n.

```csharp
Document doc = new Document(MyDir + "Id prefix.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
saveOptions.IdPrefix = "pfx1_";

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.IdPrefix.html", saveOptions);
```

### Se även

* class [HtmlFixedSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
