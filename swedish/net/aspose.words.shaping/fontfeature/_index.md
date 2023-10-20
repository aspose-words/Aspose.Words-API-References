---
title: FontFeature Enum
linktitle: FontFeature
articleTitle: FontFeature
second_title: Aspose.Words för .NET
description: Aspose.Words.Shaping.FontFeature uppräkning. Funktioner ger information om hur glyfer används i ett teckensnitt för att rendera ett skript. https//docs.microsoft.com/enus/typography/opentype/spec/featuretags i C#.
type: docs
weight: 6030
url: /sv/net/aspose.words.shaping/fontfeature/
---
## FontFeature enumeration

Funktioner ger information om hur glyfer används i ett teckensnitt för att rendera ett skript. https://docs.microsoft.com/en-us/typography/opentype/spec/featuretags

```csharp
public enum FontFeature
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| GlyphCompositionDecomposition | `1667460464` | För att minimera antalet glyferalternativ är det ibland önskvärt att dekomponera standardglyfen för ett tecken i två eller flera glyfer. Dessutom kan det vara att föredra att komponera standardglyfer för två eller flera tecken till en enda glyf för bättre glyf. processing. Den här funktionen tillåter sådan sammansättning/nedbrytning. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#ccmp Motsvarande OpenType-tagg: 'ccmp' |
| StandardLigatures | `1818847073` | Ersätter en sekvens av glyfer med en enda glyph som är att föredra för typografiska ändamål. Denna funktion täcker de ligaturer som designern/tillverkaren bedömer bör användas under normala förhållanden. Motsvarande OpenType-tagg: 'liga' https://docs .microsoft.com/en-us/typography/opentype/spec/features_ko#liga |
| RequiredLigatures | `1919707495` | Ersätter en sekvens av glyf med en enda glyf som är att föredra för typografiska ändamål. Den här funktionen täcker de ligaturer som skriptet bestämmer som krävs för att användas under normala förhållanden. Den här funktionen är viktig för vissa skript för att säkerställa korrekt glyfbildning . https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#rlig Motsvarande OpenType-tagg: 'rlig' |
| ContextualLigatures | `1668049255` | Ersätter en sekvens av glyfer med en enda glyf som är att föredra för typografiska ändamål. Till skillnad från andra ligaturfunktioner anger 'clig' sammanhanget i vilket ligaturen rekommenderas. Denna funktion är viktig i vissa skriptdesigner och för swashligaturer. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#clig Motsvarande OpenType-tagg: 'clig' |
| DiscretionaryLigatures | `1684826471` | Ersätter en sekvens av glyfer med en enda glyph som är att föredra för typografiska ändamål. Denna funktion täcker de ligaturer som kan användas för specialeffekter, enligt användarens önskemål. https://docs.microsoft.com/en-us /typography/opentype/spec/features_ae#dlig Motsvarande OpenType-tagg: 'dlig' |
| HistoricalLigatures | `1751935335` | Vissa ligaturer var i vanligt bruk tidigare, men verkar anakronistiska idag. Vissa teckensnitt inkluderar de historiska formerna som alternativ, så de kan användas för en "period"-effekt. Den här funktionen ersätter standardformerna (nuvarande) med historiska alternativ. https://docs.microsoft.com/en-us/typography/opentype/spec/features_fj#hlig Motsvarande OpenType-tagg: 'hlig' |
| ProportionalFigures | `1886287213` | Ersätter figurglyfer inställda på enhetliga (tabellformiga) bredder med motsvarande tecken inställda på glyfspecifika (proportionella) bredder. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-pnum_x000 Motsvarande OpenType-tagg: 'pnum' |
| TabularFigures | `1953396077` | Ersätter figurglyfer inställda på proportionella bredder med motsvarande tecken inställda på enhetliga (tabellformiga) bredder. Tabellbredder kommer i allmänhet att vara standard, men detta kan inte säkert antas. Naturligtvis skulle den här funktionen inte finnas i monospaced design._x000 ://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-tnum Motsvarande OpenType-tagg: 'tnum' |
| LiningFigures | `1819178349` | Den här funktionen ändrar utvalda figurer utan foder till foderfigurer. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#lnum Ekvivalent OpenType-tagg: 'lnum' |
| OldstyleFigures | `1869509997` | Den här funktionen ändrar valda figurer från standard- eller foderstil till oldstyle-form. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#onum Motsvarande OpenType-tagg: 'onum' |
| VerticalAlternates | `1986359924` | Omvandlar standardglyfer till glyfer som är lämpliga för upprätt presentation i vertikalt skrivläge. https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vert Ekvivalent OpenType-tagg: 'vert' |
| VerticalAlternatesAndRotation | `1987212338` | Ersätter vissa glyfer med fast bredd (halv-, tredje- eller kvartsbredd) eller proportionell bredd (mest latin eller katakana) med former som är lämpliga för vertikal skrivning (det vill säga roterade 90 grader medurs). https:// docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vrt2 Motsvarande OpenType-tagg: 'vrt2' |
| StylisticSet01 | `1936928817` | Stilistisk uppsättning 1 Förutom, eller istället för, stilistiska alternativ för individuella tecken (se "salt"-funktionen), kan vissa teckensnitt innehålla uppsättningar av stilistiska variantglyfer som motsvarar delar av teckenuppsättningen, t.ex. flera varianter för gemener i ett latinskt teckensnitt. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-ss01---ss20 Motsvarande OpenType-tagg: 'ss01' |
| StylisticSet02 | `1936928818` | Stilistisk uppsättning 2 Ekvivalent OpenType-tagg: 'ss02' |
| StylisticSet03 | `1936928819` | Stilistiskt set 3 Ekvivalent OpenType-tagg: 'ss03' |
| StylisticSet04 | `1936928820` | Stilistiskt set 4 Ekvivalent OpenType-tagg: 'ss04' |
| StylisticSet05 | `1936928821` | Stilistiskt set 5 Ekvivalent OpenType-tagg: 'ss05' |
| StylisticSet06 | `1936928822` | Stilistiskt set 6 Ekvivalent OpenType-tagg: 'ss06' |
| StylisticSet07 | `1936928823` | Stilistiskt set 7 Motsvarande OpenType-tagg: 'ss07' |
| StylisticSet08 | `1936928824` | Stilistiskt set 8 Ekvivalent OpenType-tagg: 'ss08' |
| StylisticSet09 | `1936928825` | Stilistiskt set 9 Ekvivalent OpenType-tagg: 'ss09' |
| StylisticSet10 | `1936929072` | Stilistiskt set 10 Ekvivalent OpenType-tagg: 'ss10' |
| StylisticSet11 | `1936929073` | Stilistiskt set 11 Motsvarande OpenType-tagg: 'ss11' |
| StylisticSet12 | `1936929074` | Stilistiskt set 12 Ekvivalent OpenType-tagg: 'ss12' |
| StylisticSet13 | `1936929075` | Stilistiskt set 13 Motsvarande OpenType-tagg: 'ss13' |
| StylisticSet14 | `1936929076` | Stilistiskt set 14 Motsvarande OpenType-tagg: 'ss14' |
| StylisticSet15 | `1936929077` | Stilistiskt set 15 Motsvarande OpenType-tagg: 'ss15' |
| StylisticSet16 | `1936929078` | Stilistiskt set 16 Motsvarande OpenType-tagg: 'ss16' |
| StylisticSet17 | `1936929079` | Stilistiskt set 17 Motsvarande OpenType-tagg: 'ss17' |
| StylisticSet18 | `1936929080` | Stilistiskt set 18 Motsvarande OpenType-tagg: 'ss18' |
| StylisticSet19 | `1936929081` | Stilistiskt set 19 Ekvivalent OpenType-tagg: 'ss19' |
| StylisticSet20 | `1936929328` | Stilistiskt set 20 Motsvarande OpenType-tagg: 'ss20' |
| Kerning | `1801810542` | Justerar mängden utrymme mellan tecken, i allmänhet för att ge optiskt konsekvent avstånd mellan tecken. Även om ett väldesignat typsnitt har konsekvent avstånd mellan tecken, kräver vissa teckenkombinationer justering för förbättrad läsbarhet. Förutom standardjustering i horisontell riktning, den här funktionen kan tillhandahålla storleksberoende kerningdata via enhetstabeller, "cross-stream" kerning i Y-textriktningen och justering av glyfplacering oberoende av förhandsjusteringen. Observera att den här funktionen kan gälla för körningar på mer än två glyfer, och skulle inte användas i teckensnitt med monospace. Observera också att den här funktionen inte gäller för text som ställs vertikalt. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#kern Ekvivalent OpenType-tagg: 'kern' |

### Se även

* namnutrymme [Aspose.Words.Shaping](../../aspose.words.shaping/)
* hopsättning [Aspose.Words](../../)
