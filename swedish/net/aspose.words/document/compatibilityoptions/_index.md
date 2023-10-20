---
title: Document.CompatibilityOptions
linktitle: CompatibilityOptions
articleTitle: CompatibilityOptions
second_title: Aspose.Words för .NET
description: Document CompatibilityOptions fast egendom. Ger tillgång till dokumentkompatibilitetsalternativ det vill säga användarinställningarna som anges påKompatibilitet fliken ialternativ dialog i Word i C#.
type: docs
weight: 50
url: /sv/net/aspose.words/document/compatibilityoptions/
---
## Document.CompatibilityOptions property

Ger tillgång till dokumentkompatibilitetsalternativ (det vill säga användarinställningarna som anges på**Kompatibilitet** fliken i**alternativ** dialog i Word).

```csharp
public CompatibilityOptions CompatibilityOptions { get; }
```

## Exempel

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

* class [CompatibilityOptions](../../../aspose.words.settings/compatibilityoptions/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
