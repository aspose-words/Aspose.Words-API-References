---
title: FontFeature Enum
linktitle: FontFeature
articleTitle: FontFeature
second_title: Aspose.Words für .NET
description: Aspose.Words.Shaping.FontFeature opsomming. Funktionen bieten Informationen darüber wie Glyphen in einer Schriftart zum Rendern eines Skripts verwendet werden. https//docs.microsoft.com/enus/typography/opentype/spec/featuretags in C#.
type: docs
weight: 6030
url: /de/net/aspose.words.shaping/fontfeature/
---
## FontFeature enumeration

Funktionen bieten Informationen darüber, wie Glyphen in einer Schriftart zum Rendern eines Skripts verwendet werden. https://docs.microsoft.com/en-us/typography/opentype/spec/featuretags

```csharp
public enum FontFeature
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| GlyphCompositionDecomposition | `1667460464` | Um die Anzahl der Glyphenalternativen zu minimieren, ist es manchmal wünschenswert, das Standardglyphe für ein Zeichen in zwei oder mehr Glyphen zu zerlegen. Darüber hinaus kann es für eine bessere Glyphe vorzuziehen sein, Standardglyphen für zwei oder mehr Zeichen in einem einzigen Glyphen zusammenzufassen Verarbeitung. Diese Funktion ermöglicht eine solche Zusammensetzung/Zerlegung. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#ccmp Äquivalentes OpenType-Tag: 'ccmp' |
| StandardLigatures | `1818847073` | Ersetzt eine Folge von Glyphen durch ein einzelnes Glyph, das für typografische Zwecke bevorzugt wird. Diese Funktion deckt die Ligaturen ab, die der Designer/Hersteller unter normalen Bedingungen verwenden sollte. Äquivalentes OpenType-Tag: 'liga' https://docs .microsoft.com/en-us/typography/opentype/spec/features_ko#liga |
| RequiredLigatures | `1919707495` | Ersetzt eine Folge von Glyphen durch ein einzelnes Glyph, das für typografische Zwecke bevorzugt wird. Diese Funktion deckt die Ligaturen ab, die das Skript als erforderlich für die Verwendung unter normalen Bedingungen bestimmt. Diese Funktion ist für einige Skripte wichtig, um eine korrekte Glyphenbildung sicherzustellen . https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#rlig Äquivalentes OpenType-Tag: 'rlig' |
| ContextualLigatures | `1668049255` | Ersetzt eine Folge von Glyphen durch ein einzelnes Glyph, das für typografische Zwecke bevorzugt wird. Im Gegensatz zu anderen Ligaturfunktionen gibt „clig“ den Kontext an, in dem die Ligatur empfohlen wird. Diese Funktion ist in einigen Skriptentwürfen und für Swash-Ligaturen wichtig. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#clig Äquivalentes OpenType-Tag: 'clig' |
| DiscretionaryLigatures | `1684826471` | Ersetzt eine Folge von Glyphen durch ein einzelnes Glyph, das für typografische Zwecke bevorzugt wird. Diese Funktion deckt die Ligaturen ab, die nach Wunsch des Benutzers für Spezialeffekte verwendet werden können. https://docs.microsoft.com/en-us /typography/opentype/spec/features_ae#dlig Äquivalentes OpenType-Tag: 'dlig' |
| HistoricalLigatures | `1751935335` | Einige Ligaturen wurden in der Vergangenheit häufig verwendet, erscheinen heute jedoch anachronistisch. Einige Schriftarten enthalten die historischen Formen als Alternativen, sodass sie für einen „Punkt“-Effekt verwendet werden können. Diese Funktion ersetzt die standardmäßigen (aktuellen) Formen durch die historische Alternativen. https://docs.microsoft.com/en-us/typography/opentype/spec/features_fj#hlig Äquivalentes OpenType-Tag: 'hlig' |
| ProportionalFigures | `1886287213` | Ersetzt Abbildungsglyphen, die auf einheitliche (tabellarische) Breiten festgelegt sind, durch entsprechende Glyphen, die auf glyphenspezifische (proportionale) Breiten festgelegt sind. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-pnum Äquivalentes OpenType-Tag: 'pnum' |
| TabularFigures | `1953396077` | Ersetzt Figurenglyphen, die auf proportionale Breiten eingestellt sind, durch entsprechende Glyphen, die auf einheitliche (tabellenförmige) Breiten eingestellt sind. Tabellenbreiten sind im Allgemeinen die Standardeinstellung, aber das kann nicht mit Sicherheit angenommen werden. Natürlich wäre diese Funktion in monospaced Designs nicht vorhanden. https ://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-tnum Äquivalentes OpenType-Tag: 'tnum' |
| LiningFigures | `1819178349` | Diese Funktion ändert ausgewählte nicht-linierende Figuren in linierende Figuren. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#lnum Äquivalentes OpenType-Tag: 'lnum' |
| OldstyleFigures | `1869509997` | Diese Funktion ändert ausgewählte Figuren vom Standard- oder Linienstil in die Form im alten Stil. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#onum Äquivalentes OpenType-Tag: 'onum' |
| VerticalAlternates | `1986359924` | Wandelt Standardglyphen in Glyphen um, die für die aufrechte Darstellung im vertikalen Schreibmodus geeignet sind. https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vert Äquivalentes OpenType-Tag: „vert“ |
| VerticalAlternatesAndRotation | `1987212338` | Ersetzt einige Glyphen mit fester Breite (halbe, dritte oder viertel Breite) oder proportionaler Breite (hauptsächlich Latein oder Katakana) durch Formen, die für vertikales Schreiben geeignet sind (d. h. um 90 Grad im Uhrzeigersinn gedreht). https:// docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vrt2 Äquivalentes OpenType-Tag: 'vrt2' |
| StylisticSet01 | `1936928817` | Stilsatz 1 Zusätzlich zu oder anstelle von stilistischen Alternativen einzelner Glyphen (siehe „Salt“-Funktion) können einige Schriftarten Sätze stilistischer Glyphen enthalten, die Teilen des Zeichensatzes entsprechen, z. B. mehrere Varianten für Kleinbuchstaben in eine lateinische Schriftart. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-ss01---ss20 Äquivalentes OpenType-Tag: 'ss01' |
| StylisticSet02 | `1936928818` | Stilsatz 2 Äquivalentes OpenType-Tag: 'ss02' |
| StylisticSet03 | `1936928819` | Stilsatz 3 Äquivalentes OpenType-Tag: 'ss03' |
| StylisticSet04 | `1936928820` | Stilsatz 4 Äquivalentes OpenType-Tag: 'ss04' |
| StylisticSet05 | `1936928821` | Stilset 5 Äquivalentes OpenType-Tag: 'ss05' |
| StylisticSet06 | `1936928822` | Stilsatz 6 Äquivalentes OpenType-Tag: 'ss06' |
| StylisticSet07 | `1936928823` | Stilsatz 7 Äquivalentes OpenType-Tag: 'ss07' |
| StylisticSet08 | `1936928824` | Stilsatz 8 Äquivalentes OpenType-Tag: 'ss08' |
| StylisticSet09 | `1936928825` | Stilsatz 9 Äquivalentes OpenType-Tag: 'ss09' |
| StylisticSet10 | `1936929072` | Stilsatz 10 Äquivalentes OpenType-Tag: 'ss10' |
| StylisticSet11 | `1936929073` | Stilsatz 11 Äquivalentes OpenType-Tag: 'ss11' |
| StylisticSet12 | `1936929074` | Stilsatz 12 Äquivalentes OpenType-Tag: 'ss12' |
| StylisticSet13 | `1936929075` | Stilsatz 13 Äquivalentes OpenType-Tag: 'ss13' |
| StylisticSet14 | `1936929076` | Stilsatz 14 Äquivalentes OpenType-Tag: 'ss14' |
| StylisticSet15 | `1936929077` | Stilsatz 15 Äquivalentes OpenType-Tag: 'ss15' |
| StylisticSet16 | `1936929078` | Stilsatz 16 Äquivalentes OpenType-Tag: 'ss16' |
| StylisticSet17 | `1936929079` | Stilsatz 17 Äquivalentes OpenType-Tag: 'ss17' |
| StylisticSet18 | `1936929080` | Stilsatz 18 Äquivalentes OpenType-Tag: 'ss18' |
| StylisticSet19 | `1936929081` | Stilsatz 19 Äquivalentes OpenType-Tag: 'ss19' |
| StylisticSet20 | `1936929328` | Stilsatz 20 Äquivalentes OpenType-Tag: 'ss20' |
| Kerning | `1801810542` | Passt den Abstand zwischen den Glyphen an, im Allgemeinen, um einen optisch einheitlichen Abstand zwischen den Glyphen zu gewährleisten. Obwohl eine gut gestaltete Schriftart insgesamt einen konsistenten Abstand zwischen den Glyphen aufweist, müssen einige Glyphenkombinationen angepasst werden, um die Lesbarkeit zu verbessern. Neben der Standardanpassung in horizontaler Richtung Diese Funktion kann größenabhängige Kerning-Daten über Gerätetabellen, „Cross-Stream“-Kerning in der Y-Textrichtung und Anpassung der Glyphenplatzierung unabhängig von der Vorabanpassung liefern. Beachten Sie, dass diese Funktion möglicherweise für Läufe von mehr als zwei gilt Glyphen und würde nicht in monospaced Schriftarten verwendet. Beachten Sie außerdem, dass diese Funktion nicht für vertikal gesetzten Text gilt. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#kern Äquivalent OpenType-Tag: 'kern' |

### Siehe auch

* namensraum [Aspose.Words.Shaping](../../aspose.words.shaping/)
* Montage [Aspose.Words](../../)
