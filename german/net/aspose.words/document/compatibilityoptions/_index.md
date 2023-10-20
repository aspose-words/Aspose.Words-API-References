---
title: Document.CompatibilityOptions
linktitle: CompatibilityOptions
articleTitle: CompatibilityOptions
second_title: Aspose.Words für .NET
description: Document CompatibilityOptions eigendom. Bietet Zugriff auf Dokumentkompatibilitätsoptionen d. h. die Benutzereinstellungen die im eingegeben wurden.Kompatibilität Registerkarte desOptionen Dialog in Word in C#.
type: docs
weight: 50
url: /de/net/aspose.words/document/compatibilityoptions/
---
## Document.CompatibilityOptions property

Bietet Zugriff auf Dokumentkompatibilitätsoptionen (d. h. die Benutzereinstellungen, die im eingegeben wurden).**Kompatibilität** Registerkarte des**Optionen** Dialog in Word).

```csharp
public CompatibilityOptions CompatibilityOptions { get; }
```

## Beispiele

Zeigt, wie das Dokument für verschiedene Versionen von Microsoft Word optimiert wird.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // Dieses Objekt enthält eine umfangreiche Liste von Flags, die für jedes Dokument einzigartig sind
    // die es uns ermöglichen, die Abwärtskompatibilität mit älteren Versionen von Microsoft Word zu erleichtern.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // Standardeinstellungen für ein leeres Dokument drucken.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // Auf diese Einstellungen können wir in Microsoft Word über „Datei“ -> zugreifen. „Optionen“ -> „Erweitert“ –> „Kompatibilitätsoptionen für…“.
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // Wir können die OptimizeFor-Methode verwenden, um eine optimale Kompatibilität mit einer bestimmten Microsoft Word-Version sicherzustellen.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// Gruppiert alle Flags in den Kompatibilitätsoptionen eines Dokuments nach Status und gibt dann jede Gruppe aus.
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

### Siehe auch

* class [CompatibilityOptions](../../../aspose.words.settings/compatibilityoptions/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
