---
title: TableSubstitutionRule.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words för .NET
description: Spara enkelt dina inställningar för tabellersättning med TableSubstitutionRule Save-metoden. Effektivisera din datahantering idag!
type: docs
weight: 70
url: /sv/net/aspose.words.fonts/tablesubstitutionrule/save/
---
## Save(*string*) {#save_1}

Sparar de aktuella inställningarna för tabellersättning till filen.

```csharp
public void Save(string fileName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Namn på utdatafil. |

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

---

## Save(*Stream*) {#save}

Sparar de aktuella inställningarna för tabellersättning till strömmen.

```csharp
public void Save(Stream outputStream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| outputStream | Stream | Utgångsström. |

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
