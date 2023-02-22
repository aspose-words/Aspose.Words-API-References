---
title: TableSubstitutionRule.LoadLinuxSettings
second_title: Aspose.Words för .NET API Referens
description: TableSubstitutionRule metod. Laddar fördefinierade tabellersättningsinställningar för Linuxplattformen.
type: docs
weight: 50
url: /sv/net/aspose.words.fonts/tablesubstitutionrule/loadlinuxsettings/
---
## TableSubstitutionRule.LoadLinuxSettings method

Laddar fördefinierade tabellersättningsinställningar för Linux-plattformen.

```csharp
public void LoadLinuxSettings()
```

### Exempel

Visar hur du får åtkomst till teckensnittsersättningstabeller för Windows och Linux.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Skapa en ny regel för tabellersättning och ladda standardtabellen för Microsoft Windows-teckensnittsersättning.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// I Windows är standardersättningen för "Times New Roman CE"-teckensnittet "Times New Roman".
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Vi kan spara tabellen i form av ett XML-dokument.
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// Linux har sin egen ersättningstabell.
// Det finns flera ersättningsteckensnitt för "Times New Roman CE".
// Om den första ersättningen, "FreeSerif" inte heller är tillgänglig,
// denna regel kommer att cykla genom de andra i arrayen tills den hittar en tillgänglig.
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Spara Linux-ersättningstabellen i form av ett XML-dokument med hjälp av en ström.
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### Se även

* class [TableSubstitutionRule](../)
* namnutrymme [Aspose.Words.Fonts](../../tablesubstitutionrule/)
* hopsättning [Aspose.Words](../../../)


