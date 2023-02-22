---
title: DocumentPropertyCollection.Count
second_title: Aspose.Words per .NET API Reference
description: DocumentPropertyCollection proprietà. Ottiene il numero di elementi nella raccolta.
type: docs
weight: 10
url: /it/net/aspose.words.properties/documentpropertycollection/count/
---
## DocumentPropertyCollection.Count property

Ottiene il numero di elementi nella raccolta.

```csharp
public int Count { get; }
```

### Esempi

Mostra come lavorare con le proprietà del documento personalizzate.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Ogni documento contiene una raccolta di proprietà personalizzate che, come le proprietà integrate, sono coppie chiave-valore.
// Il documento ha un elenco fisso di proprietà integrate. L'utente crea tutte le proprietà personalizzate. 
Assert.AreEqual("Value of custom document property", doc.CustomDocumentProperties["CustomProperty"].ToString());

doc.CustomDocumentProperties.Add("CustomProperty2", "Value of custom document property #2");

Console.WriteLine("Custom Properties:");
foreach (var customDocumentProperty in doc.CustomDocumentProperties)
{
    Console.WriteLine(customDocumentProperty.Name);
    Console.WriteLine($"\tType:\t{customDocumentProperty.Type}");
    Console.WriteLine($"\tValue:\t\"{customDocumentProperty.Value}\"");
}
```

### Guarda anche

* class [DocumentPropertyCollection](../)
* spazio dei nomi [Aspose.Words.Properties](../../documentpropertycollection/)
* assemblea [Aspose.Words](../../../)


