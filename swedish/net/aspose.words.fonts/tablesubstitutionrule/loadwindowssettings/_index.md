---
title: TableSubstitutionRule.LoadWindowsSettings
linktitle: LoadWindowsSettings
articleTitle: LoadWindowsSettings
second_title: Aspose.Words för .NET
description: Ladda enkelt fördefinierade tabellersättningsinställningar för Windows med metoden LoadWindowsSettings. Optimera ditt arbetsflöde idag!
type: docs
weight: 60
url: /sv/net/aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/
---
## TableSubstitutionRule.LoadWindowsSettings method

Laddar fördefinierade inställningar för tabellersättning för Windows-plattformen.

```csharp
public void LoadWindowsSettings()
```

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

* class [TableSubstitutionRule](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
