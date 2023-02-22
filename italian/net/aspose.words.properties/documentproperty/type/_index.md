---
title: DocumentProperty.Type
second_title: Aspose.Words per .NET API Reference
description: DocumentProperty proprietà. Ottiene il tipo di dati della proprietà.
type: docs
weight: 40
url: /it/net/aspose.words.properties/documentproperty/type/
---
## DocumentProperty.Type property

Ottiene il tipo di dati della proprietà.

```csharp
public PropertyType Type { get; }
```

### Esempi

Mostra come lavorare con le proprietà del documento integrate.

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

Mostra come lavorare con le proprietà personalizzate di un documento.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Le proprietà del documento personalizzate sono coppie chiave-valore che possiamo aggiungere al documento.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// La raccolta ordina le proprietà personalizzate in ordine alfabetico.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Stampa ogni proprietà personalizzata nel documento.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Visualizza il valore di una proprietà personalizzata utilizzando un campo DOCPROPERTY.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Possiamo trovare queste proprietà personalizzate in Microsoft Word tramite "File" -> "Proprietà" > "Proprietà avanzate" > "Costume".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Di seguito sono riportati tre modi per rimuovere le proprietà personalizzate da un documento.
// 1 - Rimuovi per indice:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Rimuovi per nome:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Svuota l'intera collezione in una volta:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Guarda anche

* enum [PropertyType](../../propertytype/)
* class [DocumentProperty](../)
* spazio dei nomi [Aspose.Words.Properties](../../documentproperty/)
* assemblea [Aspose.Words](../../../)


