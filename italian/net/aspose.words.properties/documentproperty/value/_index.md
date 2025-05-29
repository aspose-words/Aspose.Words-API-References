---
title: DocumentProperty.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words per .NET
description: Scopri come gestire in modo efficiente i valori DocumentProperty: recupera o aggiorna facilmente i valori delle proprietà per un maggiore controllo dei documenti e una maggiore produttività.
type: docs
weight: 50
url: /it/net/aspose.words.properties/documentproperty/value/
---
## DocumentProperty.Value property

Ottiene o imposta il valore della proprietà.

```csharp
public object Value { get; set; }
```

## Osservazioni

Non può essere`null`.

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
