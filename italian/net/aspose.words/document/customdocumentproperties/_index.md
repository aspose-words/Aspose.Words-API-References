---
title: Document.CustomDocumentProperties
linktitle: CustomDocumentProperties
articleTitle: CustomDocumentProperties
second_title: Aspose.Words per .NET
description: Esplora la proprietà CustomDocumentProperties per accedere e gestire in modo efficiente tutte le proprietà personalizzate del documento, migliorando così la funzionalità del tuo documento.
type: docs
weight: 80
url: /it/net/aspose.words/document/customdocumentproperties/
---
## Document.CustomDocumentProperties property

Restituisce una raccolta che rappresenta tutte le proprietà personalizzate del documento.

```csharp
public CustomDocumentProperties CustomDocumentProperties { get; }
```

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

* class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
