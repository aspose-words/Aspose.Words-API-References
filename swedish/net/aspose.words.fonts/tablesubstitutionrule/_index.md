---
title: TableSubstitutionRule Class
linktitle: TableSubstitutionRule
articleTitle: TableSubstitutionRule
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fonts.TableSubstitutionRule för effektiv typsnittshantering och sömlös textformatering i dina dokument.
type: docs
weight: 3490
url: /sv/net/aspose.words.fonts/tablesubstitutionrule/
---
## TableSubstitutionRule class

Regel för ersättning av tabellfonter.

För att lära dig mer, besök[Arbeta med teckensnitt](https://docs.aspose.com/words/net/working-with-fonts/) dokumentationsartikel.

```csharp
public class TableSubstitutionRule : FontSubstitutionRule
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Anger om regeln är aktiverad eller inte. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [AddSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/addsubstitutes/)(*string, params string[]*) | Lägger till ersättningsnamn för det ursprungliga teckensnittet. |
| [GetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/getsubstitutes/)(*string*) | Returnerar en array som innehåller ersättningsnamn för det angivna ursprungliga typsnittsnamnet. |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load)(*Stream*) | Läser in inställningar för tabellersättning från XML-strömmen. |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load_1)(*string*) | Laddar inställningar för tabellersättning från XML-fil. |
| [LoadAndroidSettings](../../aspose.words.fonts/tablesubstitutionrule/loadandroidsettings/)() | Laddar fördefinierade inställningar för tabellersättning för Android-plattformen. |
| [LoadLinuxSettings](../../aspose.words.fonts/tablesubstitutionrule/loadlinuxsettings/)() | Laddar fördefinierade inställningar för tabellersättning för Linux-plattformen. |
| [LoadWindowsSettings](../../aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/)() | Laddar fördefinierade inställningar för tabellersättning för Windows-plattformen. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save)(*Stream*) | Sparar de aktuella inställningarna för tabellersättning till strömmen. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save_1)(*string*) | Sparar de aktuella inställningarna för tabellersättning till filen. |
| [SetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/setsubstitutes/)(*string, params string[]*) | Åsidosätt ersättningsteckensnittsnamn för angivet originalteckensnittsnamn. |

## Anmärkningar

Denna regel definierar listan över ersättningsteckensnitt som ska användas om originalteckensnittet inte är tillgängligt. Ersättningar kommer att kontrolleras för teckensnittsnamnet och[`AltName`](../fontinfo/altname/) (om någon).

## Exempel

Visar hur man får åtkomst till tabeller för teckensnittsersättning för Windows och Linux.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Skapa en ny regel för tabellersättning och ladda standardtabellen för Microsoft Windows-teckensnittsersättning.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// I Windows är standardersättningen för teckensnittet "Times New Roman CE" "Times New Roman".
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Vi kan spara tabellen i form av ett XML-dokument.
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// Linux har sin egen substitutionstabell.
// Det finns flera ersättningstypsnitt för "Times New Roman CE".
// Om den första ersättningen, "FreeSerif", inte heller är tillgänglig,
// den här regeln kommer att cykla igenom de andra i arrayen tills den hittar en tillgänglig regel.
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Spara Linux-substitutionstabellen i form av ett XML-dokument med hjälp av en ström.
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### Se även

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)
