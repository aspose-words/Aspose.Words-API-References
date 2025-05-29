---
title: HtmlLoadOptions.SupportFontFaceRules
linktitle: SupportFontFaceRules
articleTitle: SupportFontFaceRules
second_title: Aspose.Words för .NET
description: Upptäck HtmlLoadOptions SupportFontFaceRules, kontrollera enkelt inläsning av teckensnitt. Förbättra din webbdesign genom att aktivera anpassade teckensnitt för ett elegant utseende.
type: docs
weight: 60
url: /sv/net/aspose.words.loading/htmlloadoptions/supportfontfacerules/
---
## HtmlLoadOptions.SupportFontFaceRules property

Hämtar eller ställer in ett värde som anger om @font-face-regler ska stödjas och om deklarerade teckensnitt ska läsas in. Standardvärdet är`falsk` .

```csharp
public bool SupportFontFaceRules { get; set; }
```

## Anmärkningar

Om det här alternativet är aktiverat laddas och bäddas teckensnitt som deklareras i @font-face-regler in i det resulterande dokumentets teckensnittsdefinitioner (se[`FontInfos`](../../../aspose.words/documentbase/fontinfos/) ). Detta gör de laddade teckensnitten tillgängliga för rendering, men aktiverar inte automatiskt inbäddning av teckensnitten när de sparas. För att spara dokumentet med laddade teckensnitt, [`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) egendomen tillhörande[`FontInfos`](../../../aspose.words/documentbase/fontinfos/) -samlingen ska vara inställd på`sann` .

Typsnittsformat som stöds är TTF, EOT och WOFF.

@font-face-regler stöds inte vid inläsning av SVG-bilder.

## Exempel

Visar hur man laddar deklarerade "@font-face"-regler.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();
loadOptions.SupportFontFaceRules = true;
Document doc = new Document(MyDir + "Html with FontFace.html", loadOptions);

Assert.AreEqual("Squarish Sans CT Regular", doc.FontInfos[0].Name);
```

### Se även

* class [HtmlLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
