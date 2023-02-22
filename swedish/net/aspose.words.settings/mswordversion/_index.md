---
title: Enum MsWordVersion
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Settings.MsWordVersion uppräkning. Tillåter Aspose.Wods att efterlikna MS Wordversionsspecifikt programbeteende.
type: docs
weight: 5560
url: /sv/net/aspose.words.settings/mswordversion/
---
## MsWordVersion enumeration

Tillåter Aspose.Wods att efterlikna MS Word-versionsspecifikt programbeteende.

```csharp
public enum MsWordVersion
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Word2000 | `0` | Optimera Aspose.Words-beteendet för att matcha MS Word 2000-versionen. |
| Word2002 | `1` | Optimera Aspose.Words-beteendet för att matcha MS Word 2002-versionen. |
| Word2003 | `2` | Optimera Aspose.Words-beteendet för att matcha MS Word 2003-versionen. |
| Word2007 | `3` | Optimera Aspose.Words-beteendet för att matcha MS Word 2007-versionen. |
| Word2010 | `4` | Optimera Aspose.Words beteende för att matcha MS Word 2010 version. |
| Word2013 | `5` | Optimera Aspose.Words-beteendet för att matcha MS Word 2013-versionen. |
| Word2016 | `6` | Optimera Aspose.Words-beteendet för att matcha MS Word 2016-versionen. |
| Word2019 | `7` | Optimera Aspose.Words-beteendet för att matcha MS Word 2019-versionen. |

### Exempel

Visar hur man optimerar dokumentet för olika versioner av Microsoft Word.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // Detta objekt innehåller en omfattande lista med flaggor som är unika för varje dokument
    // som tillåter oss att underlätta bakåtkompatibilitet med äldre versioner av Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // Skriv ut standardinställningarna för ett tomt dokument.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // Vi kan komma åt dessa inställningar i Microsoft Word via "File" -> "Alternativ" -> "Avancerat" -> "Kompatibilitetsalternativ för...".
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // Vi kan använda OptimizeFor-metoden för att säkerställa optimal kompatibilitet med en specifik Microsoft Word-version.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// Grupperar alla flaggor i ett dokuments kompatibilitetsalternativobjekt efter tillstånd och skrivs sedan ut varje grupp.
/// </summary>
private static void PrintCompatibilityOptions(CompatibilityOptions options)
{
    for (int i = 1; i >= 0; i--)
    {
        Console.WriteLine(Convert.ToBoolean(i) ? "\tEnabled options:" : "\tDisabled options:");
        SortedSet<string> optionNames = new SortedSet<string>();

        foreach (System.ComponentModel.PropertyDescriptor descriptor in System.ComponentModel.TypeDescriptor.GetProperties(options))
        {
            if (descriptor.PropertyType == Type.GetType("System.Boolean") && i == Convert.ToInt32(descriptor.GetValue(options)))
            {
                optionNames.Add(descriptor.Name);
            }
        }

        foreach (string s in optionNames)
        {
            Console.WriteLine($"\t\t{s}");
        }
    }
}
```

### Se även

* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)


