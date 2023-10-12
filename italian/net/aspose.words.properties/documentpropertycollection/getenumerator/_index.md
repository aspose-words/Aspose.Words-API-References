---
title: DocumentPropertyCollection.GetEnumerator
second_title: Aspose.Words per .NET API Reference
description: DocumentPropertyCollection metodo. Restituisce un oggetto enumeratore che può essere utilizzato per scorrere tutti gli elementi della raccolta.
type: docs
weight: 50
url: /it/net/aspose.words.properties/documentpropertycollection/getenumerator/
---
## DocumentPropertyCollection.GetEnumerator method

Restituisce un oggetto enumeratore che può essere utilizzato per scorrere tutti gli elementi della raccolta.

```csharp
public IEnumerator<DocumentProperty> GetEnumerator()
```

### Esempi

Mostra come utilizzare le proprietà personalizzate di un documento.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Le proprietà personalizzate del documento sono coppie chiave-valore che possiamo aggiungere al documento.
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

// 3 - Svuota l'intera raccolta in una volta:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Guarda anche

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* spazio dei nomi [Aspose.Words.Properties](../../documentpropertycollection/)
* assemblea [Aspose.Words](../../../)


