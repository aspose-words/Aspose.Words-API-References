---
title: DocumentProperty Class
linktitle: DocumentProperty
articleTitle: DocumentProperty
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Properties.DocumentProperty per gestire in modo efficiente le proprietà dei documenti, sia personalizzate che integrate. Migliora la gestione dei tuoi documenti oggi stesso!
type: docs
weight: 5200
url: /it/net/aspose.words.properties/documentproperty/
---
## DocumentProperty class

Rappresenta una proprietà personalizzata o incorporata del documento.

Per saperne di più, visita il[Lavorare con le proprietà del documento](https://docs.aspose.com/words/net/work-with-document-properties/) articolo di documentazione.

```csharp
public class DocumentProperty
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [IsLinkToContent](../../aspose.words.properties/documentproperty/islinktocontent/) { get; } | Indica se questa proprietà è collegata al contenuto o meno. |
| [LinkSource](../../aspose.words.properties/documentproperty/linksource/) { get; } | Ottiene la fonte di una proprietà di documento personalizzata collegata. |
| [Name](../../aspose.words.properties/documentproperty/name/) { get; } | Restituisce il nome della proprietà. |
| [Type](../../aspose.words.properties/documentproperty/type/) { get; } | Ottiene il tipo di dati della proprietà. |
| [Value](../../aspose.words.properties/documentproperty/value/) { get; set; } | Ottiene o imposta il valore della proprietà. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [ToBool](../../aspose.words.properties/documentproperty/tobool/)() | Restituisce il valore della proprietà come bool. |
| [ToByteArray](../../aspose.words.properties/documentproperty/tobytearray/)() | Restituisce il valore della proprietà come array di byte. |
| [ToDateTime](../../aspose.words.properties/documentproperty/todatetime/)() | Restituisce il valore della proprietà come**Data e ora** in UTC. |
| [ToDouble](../../aspose.words.properties/documentproperty/todouble/)() | Restituisce il valore della proprietà come double. |
| [ToInt](../../aspose.words.properties/documentproperty/toint/)() | Restituisce il valore della proprietà come intero. |
| override [ToString](../../aspose.words.properties/documentproperty/tostring/)() | Restituisce il valore della proprietà come stringa formattata in base alle impostazioni locali correnti. |

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

* class [DocumentPropertyCollection](../documentpropertycollection/)
* spazio dei nomi [Aspose.Words.Properties](../../aspose.words.properties/)
* assemblea [Aspose.Words](../../)
