---
title: FontFeature Enum
linktitle: FontFeature
articleTitle: FontFeature
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.Shaping.FontFeature, die die Verwendung von Glyphen in Schriftarten für die Skriptdarstellung detailliert beschreibt. Erweitern Sie noch heute Ihr Typografie-Wissen!
type: docs
weight: 6860
url: /de/net/aspose.words.shaping/fontfeature/
---
## FontFeature enumeration

Funktionen liefern Informationen darüber, wie Glyphen in einer Schriftart verwendet werden, um ein Skript darzustellen. https://docs.microsoft.com/en-us/typography/opentype/spec/featuretags

```csharp
public enum FontFeature
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| GlyphCompositionDecomposition | `1667460464` | Um die Anzahl der Glyphenalternativen zu minimieren, ist es manchmal wünschenswert, die Standardglyphe für ein Zeichen in zwei oder mehr Glyphen zu zerlegen. Darüber hinaus kann es vorzuziehen sein, Standardglyphen für zwei oder mehr Zeichen zu einer einzigen Glyphe zusammenzusetzen, um die Glyphenverarbeitung zu verbessern. Diese Funktion ermöglicht eine solche Zusammensetzung/Zerlegung. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#ccmp Äquivalentes OpenType-Tag: „ccmp“ |
| StandardLigatures | `1818847073` | Ersetzt eine Folge von Glyphen durch eine einzelne Glyphe, die aus typografischen Gründen bevorzugt wird. Diese Funktion umfasst die Ligaturen, die nach Ansicht des Designers/Herstellers unter normalen Bedingungen verwendet werden sollten. Äquivalentes OpenType-Tag: „liga“ https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#liga |
| RequiredLigatures | `1919707495` | Ersetzt eine Folge von Glyphen durch eine einzelne Glyphe, die aus typografischen Gründen bevorzugt wird. Diese Funktion deckt die Ligaturen ab, die das Skript unter normalen Bedingungen als erforderlich festlegt. Diese Funktion ist für einige Skripte wichtig, um die korrekte Glyphenbildung sicherzustellen. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#rlig Äquivalentes OpenType-Tag: „rlig“ |
| ContextualLigatures | `1668049255` | Ersetzt eine Folge von Glyphen durch eine einzelne Glyphe, was aus typografischen Gründen bevorzugt wird. Im Gegensatz zu anderen Ligaturfunktionen gibt „clig“ den Kontext an, in dem die Ligatur empfohlen wird. Diese Funktion ist bei einigen Skriptdesigns und für Schwungligaturen wichtig. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#clig Äquivalentes OpenType-Tag: „clig“ |
| DiscretionaryLigatures | `1684826471` | Ersetzt eine Folge von Glyphen durch eine einzelne Glyphe, die aus typografischen Gründen bevorzugt wird. Diese Funktion umfasst die Ligaturen, die je nach Benutzerwunsch für Spezialeffekte verwendet werden können. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#dlig Äquivalentes OpenType-Tag: „dlig“ |
| HistoricalLigatures | `1751935335` | Einige Ligaturen waren früher gebräuchlich, wirken heute jedoch anachronistisch. Einige Schriftarten enthalten die historischen Formen als Alternativen, sodass sie für einen „zeitgemäßen“ Effekt verwendet werden können. Diese Funktion ersetzt die (aktuellen) Standardformen durch die historischen Alternativen. https://docs.microsoft.com/en-us/typography/opentype/spec/features_fj#hlig Äquivalentes OpenType-Tag: „hlig“ |
| ProportionalFigures | `1886287213` | Ersetzt Ziffernglyphen mit einheitlicher (tabellarischer) Breite durch entsprechende Glyphen mit glyphenspezifischer (proportionaler) Breite. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-pnum Äquivalentes OpenType-Tag: „pnum“ |
| TabularFigures | `1953396077` | Ersetzt auf proportionale Breiten eingestellte Ziffernglyphen durch entsprechende Glyphen mit einheitlicher (tabellarischer) Breite. Tabellarische Breiten sind im Allgemeinen die Standardeinstellung, dies kann jedoch nicht mit Sicherheit angenommen werden. Natürlich wäre diese Funktion in monospaced Designs nicht vorhanden. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-tnum Äquivalentes OpenType-Tag: „tnum“ |
| LiningFigures | `1819178349` | Diese Funktion ändert ausgewählte nicht-linierte Ziffern in linierte Ziffern. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#lnum Äquivalentes OpenType-Tag: „lnum“ |
| OldstyleFigures | `1869509997` | Diese Funktion ändert ausgewählte Ziffern vom Standard- oder Linienstil in die Oldstyle-Form. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#onum Äquivalentes OpenType-Tag: „onum“ |
| VerticalAlternates | `1986359924` | Wandelt Standardglyphen in Glyphen um, die für die aufrechte Darstellung im vertikalen Schreibmodus geeignet sind. https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vert Äquivalentes OpenType-Tag: „vert“ |
| VerticalAlternatesAndRotation | `1987212338` | Ersetzt einige Glyphen mit fester Breite (halbe, Drittel- oder Viertelbreite) oder proportionaler Breite (meistens Latein oder Katakana) durch Formen, die für vertikales Schreiben geeignet sind (d. h. um 90 Grad im Uhrzeigersinn gedreht). https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vrt2 Äquivalentes OpenType-Tag: „vrt2“ |
| StylisticSet01 | `1936928817` | Stilistischer Satz 1 Zusätzlich zu oder anstelle von stilistischen Alternativen einzelner Glyphen (siehe „Salt“-Funktion) können einige Schriftarten Sätze stilistischer Glyphenvarianten enthalten, die Teilen des Zeichensatzes entsprechen, z. B. mehrere Varianten für Kleinbuchstaben in einer lateinischen Schriftart. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-ss01---ss20 Entsprechendes OpenType-Tag: „ss01“ |
| StylisticSet02 | `1936928818` | Stilsatz 2 Äquivalentes OpenType-Tag: „ss02“ |
| StylisticSet03 | `1936928819` | Stilsatz 3 Äquivalentes OpenType-Tag: „ss03“ |
| StylisticSet04 | `1936928820` | Stilsatz 4 Äquivalentes OpenType-Tag: „ss04“ |
| StylisticSet05 | `1936928821` | Stilsatz 5 Äquivalentes OpenType-Tag: „ss05“ |
| StylisticSet06 | `1936928822` | Stilsatz 6 Äquivalentes OpenType-Tag: „ss06“ |
| StylisticSet07 | `1936928823` | Stilistischer Satz 7 Äquivalentes OpenType-Tag: „ss07“ |
| StylisticSet08 | `1936928824` | Stilistischer Satz 8 Äquivalentes OpenType-Tag: „ss08“ |
| StylisticSet09 | `1936928825` | Stilistischer Satz 9 Äquivalentes OpenType-Tag: „ss09“ |
| StylisticSet10 | `1936929072` | Stilistischer Satz 10 Äquivalentes OpenType-Tag: „ss10“ |
| StylisticSet11 | `1936929073` | Stilistischer Satz 11 Äquivalentes OpenType-Tag: „ss11“ |
| StylisticSet12 | `1936929074` | Stilistischer Satz 12 Äquivalentes OpenType-Tag: „ss12“ |
| StylisticSet13 | `1936929075` | Stilistischer Satz 13 Äquivalentes OpenType-Tag: „ss13“ |
| StylisticSet14 | `1936929076` | Stilistischer Satz 14 Äquivalentes OpenType-Tag: „ss14“ |
| StylisticSet15 | `1936929077` | Stilistischer Satz 15 Äquivalentes OpenType-Tag: „ss15“ |
| StylisticSet16 | `1936929078` | Stilistischer Satz 16 Äquivalentes OpenType-Tag: „ss16“ |
| StylisticSet17 | `1936929079` | Stilistischer Satz 17 Äquivalentes OpenType-Tag: „ss17“ |
| StylisticSet18 | `1936929080` | Stilistischer Satz 18 Äquivalentes OpenType-Tag: „ss18“ |
| StylisticSet19 | `1936929081` | Stilistischer Satz 19 Äquivalentes OpenType-Tag: „ss19“ |
| StylisticSet20 | `1936929328` | Stilistischer Satz 20 Äquivalentes OpenType-Tag: „ss20“ |
| Kerning | `1801810542` | Passt den Abstand zwischen Glyphen an, um im Allgemeinen einen optisch konsistenten Abstand zwischen den Glyphen zu gewährleisten. Obwohl eine gut gestaltete Schriftart insgesamt einen konsistenten Abstand zwischen den Glyphen aufweist, müssen einige Glyphenkombinationen zur besseren Lesbarkeit angepasst werden. Neben der Standardanpassung in horizontaler Richtung kann diese Funktion größenabhängige Kerning-Daten über Gerätetabellen bereitstellen, „Cross-Stream“-Kerning in Y-Textrichtung und die Anpassung der Glyphenplatzierung unabhängig von der erweiterten Anpassung. Beachten Sie, dass diese Funktion für Läufe mit mehr als zwei Glyphen gelten kann und nicht in Monospace-Schriftarten verwendet wird. Beachten Sie außerdem, dass diese Funktion nicht für vertikal gesetzten Text gilt. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#kern Äquivalentes OpenType-Tag: „kern“ |

### Siehe auch

* namensraum [Aspose.Words.Shaping](../../aspose.words.shaping/)
* Montage [Aspose.Words](../../)
