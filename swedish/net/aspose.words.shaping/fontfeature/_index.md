---
title: FontFeature Enum
linktitle: FontFeature
articleTitle: FontFeature
second_title: Aspose.Words för .NET
description: Upptäck enumereringen Aspose.Words.Shaping.FontFeature, som beskriver användningen av teckensnitt i skriptrendering. Förbättra dina kunskaper om typografi idag!
type: docs
weight: 6860
url: /sv/net/aspose.words.shaping/fontfeature/
---
## FontFeature enumeration

Funktioner ger information om hur tecken används i ett teckensnitt för att rendera ett skript. https://docs.microsoft.com/en-us/typography/opentype/spec/featuretags

```csharp
public enum FontFeature
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| GlyphCompositionDecomposition | `1667460464` | För att minimera antalet alternativa teckentecken är det ibland önskvärt att dela upp standardteckenteckenet för ett tecken i två eller fler teckentecken. Dessutom kan det vara att föredra att komponera standardteckentecken för två eller fler tecken till ett enda tecken för bättre teckenbearbetning. Den här funktionen möjliggör sådan komposition/nedbrytning. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#ccmp Motsvarande OpenType-tagg: 'ccmp' |
| StandardLigatures | `1818847073` | Ersätter en sekvens av tecken med en enda teckengrupp som föredras för typografiska ändamål. Denna funktion täcker de ligaturer som designern/tillverkaren bedömer bör användas under normala förhållanden. Motsvarande OpenType-tagg: 'liga' https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#liga |
| RequiredLigatures | `1919707495` | Ersätter en sekvens av tecken med en enda teckengrupp som föredras för typografiska ändamål. Den här funktionen täcker de ligaturer som skriptet anser vara nödvändiga för användning under normala förhållanden. Den här funktionen är viktig för vissa skript för att säkerställa korrekt teckenformation. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#rlig Motsvarande OpenType-tagg: 'rlig' |
| ContextualLigatures | `1668049255` | Ersätter en sekvens av tecken med en enda teckentyp, vilket är att föredra för typografiska ändamål. Till skillnad från andra ligaturfunktioner anger 'clig' det sammanhang där ligaturen rekommenderas. Denna funktion är viktig i vissa skriptdesigner och för swash-ligaturer. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#clig Motsvarande OpenType-tagg: 'clig' |
| DiscretionaryLigatures | `1684826471` | Ersätter en sekvens av tecken med en enda teckentyp som föredras för typografiska ändamål. Den här funktionen täcker de ligaturer som kan användas för specialeffekter, enligt användarens önskemål. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#dlig Motsvarande OpenType-tagg: 'dlig' |
| HistoricalLigatures | `1751935335` | Vissa ligaturer var vanliga förr i tiden, men framstår som anakronistiska idag. Vissa teckensnitt inkluderar de historiska formerna som alternativ, så de kan användas för en "punkt"-effekt. Den här funktionen ersätter standardformerna (nuvarande) med de historiska alternativen. https://docs.microsoft.com/en-us/typography/opentype/spec/features_fj#hlig Motsvarande OpenType-tagg: 'hlig' |
| ProportionalFigures | `1886287213` | Ersätter figurtecken som är inställda på enhetliga (tabulära) bredder med motsvarande tecken som är inställda på teckenspecifika (proportionella) bredder. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-pnum Motsvarande OpenType-tagg: 'pnum' |
| TabularFigures | `1953396077` | Ersätter figurtecken som är inställda på proportionella bredder med motsvarande tecken som är inställda på enhetliga (tabulära) bredder. Tabellära bredder är generellt standard, men detta kan inte antas med säkerhet. Naturligtvis skulle den här funktionen inte finnas i design med monospace. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-tnum Motsvarande OpenType-tagg: 'tnum' |
| LiningFigures | `1819178349` | Den här funktionen ändrar valda icke-linjeformade figurer till linjeformade figurer. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#lnum Motsvarande OpenType-tagg: 'lnum' |
| OldstyleFigures | `1869509997` | Den här funktionen ändrar valda figurer från standard- eller linjestilen till gammaldags form. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#onum Motsvarande OpenType-tagg: 'onum' |
| VerticalAlternates | `1986359924` | Omvandlar standardtecken till tecken som är lämpliga för upprätt presentation i vertikalt skrivläge. https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vert Motsvarande OpenType-tagg: 'vert' |
| VerticalAlternatesAndRotation | `1987212338` | Ersätter vissa tecken med fast bredd (halv-, tredje- eller fjärdedelsbredd) eller proportionell bredd (mestadels latin eller katakana) med former som är lämpliga för vertikal skrivning (det vill säga roterade 90 grader medurs). https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vrt2 Motsvarande OpenType-tagg: 'vrt2' |
| StylisticSet01 | `1936928817` | Stilistisk uppsättning 1 Utöver, eller istället för, stilistiska alternativ till enskilda tecken (se 'salt'-funktionen), kan vissa teckensnitt innehålla uppsättningar av stilistiska varianttecken som motsvarar delar av teckenuppsättningen, t.ex. flera varianter för gemener i ett latinskt teckensnitt. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-ss01---ss20 Motsvarande OpenType-tagg: 'ss01' |
| StylisticSet02 | `1936928818` | Stilistisk uppsättning 2 Motsvarande OpenType-tagg: 'ss02' |
| StylisticSet03 | `1936928819` | Stilistisk uppsättning 3 Motsvarande OpenType-tagg: 'ss03' |
| StylisticSet04 | `1936928820` | Stilistisk uppsättning 4 Motsvarande OpenType-tagg: 'ss04' |
| StylisticSet05 | `1936928821` | Stilistisk uppsättning 5 Motsvarande OpenType-tagg: 'ss05' |
| StylisticSet06 | `1936928822` | Stilistisk uppsättning 6 Motsvarande OpenType-tagg: 'ss06' |
| StylisticSet07 | `1936928823` | Stilistisk uppsättning 7 Motsvarande OpenType-tagg: 'ss07' |
| StylisticSet08 | `1936928824` | Stilistisk uppsättning 8 Motsvarande OpenType-tagg: 'ss08' |
| StylisticSet09 | `1936928825` | Stilistisk uppsättning 9 Motsvarande OpenType-tagg: 'ss09' |
| StylisticSet10 | `1936929072` | Stilistisk uppsättning 10 Motsvarande OpenType-tagg: 'ss10' |
| StylisticSet11 | `1936929073` | Stilistisk uppsättning 11 Motsvarande OpenType-tagg: 'ss11' |
| StylisticSet12 | `1936929074` | Stilistisk uppsättning 12 Motsvarande OpenType-tagg: 'ss12' |
| StylisticSet13 | `1936929075` | Stilistisk uppsättning 13 Motsvarande OpenType-tagg: 'ss13' |
| StylisticSet14 | `1936929076` | Stilistisk uppsättning 14 Motsvarande OpenType-tagg: 'ss14' |
| StylisticSet15 | `1936929077` | Stilistisk uppsättning 15 Motsvarande OpenType-tagg: 'ss15' |
| StylisticSet16 | `1936929078` | Stilistisk uppsättning 16 Motsvarande OpenType-tagg: 'ss16' |
| StylisticSet17 | `1936929079` | Stilistisk uppsättning 17 Motsvarande OpenType-tagg: 'ss17' |
| StylisticSet18 | `1936929080` | Stilistisk uppsättning 18 Motsvarande OpenType-tagg: 'ss18' |
| StylisticSet19 | `1936929081` | Stilistisk uppsättning 19 Motsvarande OpenType-tagg: 'ss19' |
| StylisticSet20 | `1936929328` | Stilistisk uppsättning 20 Motsvarande OpenType-tagg: 'ss20' |
| Kerning | `1801810542` | Justerar mängden avstånd mellan tecken, generellt för att ge optiskt konsekvent avstånd mellan tecken. Även om ett väl utformat typsnitt har konsekvent avstånd mellan tecken totalt sett, kräver vissa teckenkombinationer justering för förbättrad läsbarhet. Förutom standardjustering i horisontell riktning kan den här funktionen tillhandahålla storleksberoende kerningdata via enhetstabeller, "tvärströms"-kerning i Y-textriktningen och justering av teckenplacering oberoende av den avancerade justeringen. Observera att den här funktionen kan gälla för serier med mer än två tecken och inte skulle användas i teckensnitt med fast radavstånd. Observera också att den här funktionen inte gäller text som är vertikalt inställd. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#kern Motsvarande OpenType-tagg: 'kern' |

### Se även

* namnutrymme [Aspose.Words.Shaping](../../aspose.words.shaping/)
* hopsättning [Aspose.Words](../../)
