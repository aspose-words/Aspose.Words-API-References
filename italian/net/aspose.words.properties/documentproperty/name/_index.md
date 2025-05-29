---
title: DocumentProperty.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words per .NET
description: Scopri la funzionalità DocumentProperty Name che recupera senza sforzo i nomi delle proprietà, migliorando la gestione dei documenti e l'efficienza del flusso di lavoro.
type: docs
weight: 30
url: /it/net/aspose.words.properties/documentproperty/name/
---
## DocumentProperty.Name property

Restituisce il nome della proprietà.

```csharp
public string Name { get; }
```

## Osservazioni

Non può essere`null` e non può essere una stringa vuota.

## Esempi

Mostra come lavorare con le proprietà integrate del documento.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// L'oggetto "Documento" contiene alcuni dei suoi metadati nei suoi membri.
Console.WriteLine($"Document filename:\n\t \"{doc.OriginalFileName}\"");

// Il documento memorizza anche i metadati nelle sue proprietà integrate.
// Ogni proprietà incorporata è un membro dell'oggetto "BuiltInDocumentProperties" del documento.
Console.WriteLine("Built-in Properties:");
foreach (DocumentProperty docProperty in doc.BuiltInDocumentProperties)
{
    Console.WriteLine(docProperty.Name);
    Console.WriteLine($"\tType:\t{docProperty.Type}");

    // Alcune proprietà possono memorizzare più valori.
    if (docProperty.Value is ICollection<object>)
    {
        foreach (object value in docProperty.Value as ICollection<object>)
            Console.WriteLine($"\tValue:\t\"{value}\"");
    }
    else
    {
        Console.WriteLine($"\tValue:\t\"{docProperty.Value}\"");
    }
}
```

### Guarda anche

* class [DocumentProperty](../)
* spazio dei nomi [Aspose.Words.Properties](../../../aspose.words.properties/)
* assemblea [Aspose.Words](../../../)
