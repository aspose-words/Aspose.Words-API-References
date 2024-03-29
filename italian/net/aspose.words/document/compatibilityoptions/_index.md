---
title: Document.CompatibilityOptions
linktitle: CompatibilityOptions
articleTitle: CompatibilityOptions
second_title: Aspose.Words per .NET
description: Document CompatibilityOptions proprietà. Fornisce laccesso alle opzioni di compatibilità del documento ovvero le preferenze dellutente immesse nel fileCompatibilità scheda delOpzioni finestra di dialogo in Word in C#.
type: docs
weight: 50
url: /it/net/aspose.words/document/compatibilityoptions/
---
## Document.CompatibilityOptions property

Fornisce l'accesso alle opzioni di compatibilità del documento (ovvero, le preferenze dell'utente immesse nel file**Compatibilità** scheda del**Opzioni** finestra di dialogo in Word).

```csharp
public CompatibilityOptions CompatibilityOptions { get; }
```

## Esempi

Mostra come ottimizzare il documento per diverse versioni di Microsoft Word.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // Questo oggetto contiene un elenco completo di flag univoci per ciascun documento
    // che ci consentono di facilitare la compatibilità con le versioni precedenti di Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // Stampa le impostazioni predefinite per un documento vuoto.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // Possiamo accedere a queste impostazioni in Microsoft Word tramite "File" -> "Opzioni" -> "Avanzate" -> "Opzioni di compatibilità per...".
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // Possiamo utilizzare il metodo OptimizeFor per garantire la compatibilità ottimale con una versione specifica di Microsoft Word.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// Raggruppa tutti i flag nell'oggetto delle opzioni di compatibilità di un documento in base allo stato, quindi stampa ciascun gruppo.
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

### Guarda anche

* class [CompatibilityOptions](../../../aspose.words.settings/compatibilityoptions/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
