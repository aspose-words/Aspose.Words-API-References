---
title: Enum MsWordVersion
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Settings.MsWordVersion enum. Consente ad Aspose.Wods di imitare il comportamento dellapplicazione specifico della versione di MS Word.
type: docs
weight: 5560
url: /it/net/aspose.words.settings/mswordversion/
---
## MsWordVersion enumeration

Consente ad Aspose.Wods di imitare il comportamento dell'applicazione specifico della versione di MS Word.

```csharp
public enum MsWordVersion
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Word2000 | `0` | Ottimizza il comportamento di Aspose.Words in modo che corrisponda alla versione di MS Word 2000. |
| Word2002 | `1` | Ottimizza il comportamento di Aspose.Words in modo che corrisponda alla versione di MS Word 2002. |
| Word2003 | `2` | Ottimizza il comportamento di Aspose.Words in modo che corrisponda alla versione di MS Word 2003. |
| Word2007 | `3` | Ottimizza il comportamento di Aspose.Words in modo che corrisponda alla versione di MS Word 2007. |
| Word2010 | `4` | Ottimizza il comportamento di Aspose.Words in modo che corrisponda alla versione di MS Word 2010. |
| Word2013 | `5` | Ottimizza il comportamento di Aspose.Words in modo che corrisponda alla versione di MS Word 2013. |
| Word2016 | `6` | Ottimizza il comportamento di Aspose.Words in modo che corrisponda alla versione di MS Word 2016. |
| Word2019 | `7` | Ottimizza il comportamento di Aspose.Words in modo che corrisponda alla versione di MS Word 2019. |

### Esempi

Mostra come ottimizzare il documento per diverse versioni di Microsoft Word.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // Questo oggetto contiene un ampio elenco di flag univoci per ogni documento
    // che ci consentono di facilitare la compatibilità con le versioni precedenti di Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // Stampa le impostazioni predefinite per un documento vuoto.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // Possiamo accedere a queste impostazioni in Microsoft Word tramite "File" -> "Opzioni" -> "Avanzate" -> "Opzioni di compatibilità per...".
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // Possiamo utilizzare il metodo OptimizeFor per garantire la compatibilità ottimale con una specifica versione di Microsoft Word.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// Raggruppa tutti i flag nelle opzioni di compatibilità di un documento oggetto per stato, quindi stampa ogni gruppo.
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

* spazio dei nomi [Aspose.Words.Settings](../../aspose.words.settings/)
* assemblea [Aspose.Words](../../)


