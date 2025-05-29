---
title: DocumentPropertyCollection Class
linktitle: DocumentPropertyCollection
articleTitle: DocumentPropertyCollection
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Properties.DocumentPropertyCollection, il tuo punto di riferimento per gestire in modo efficiente le proprietà dei documenti predefinite e personalizzate.
type: docs
weight: 5210
url: /it/net/aspose.words.properties/documentpropertycollection/
---
## DocumentPropertyCollection class

Classe base per[`BuiltInDocumentProperties`](../builtindocumentproperties/) E[`CustomDocumentProperties`](../customdocumentproperties/) collezioni.

Per saperne di più, visita il[Lavorare con le proprietà del documento](https://docs.aspose.com/words/net/work-with-document-properties/) articolo di documentazione.

```csharp
public abstract class DocumentPropertyCollection : IEnumerable<DocumentProperty>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.properties/documentpropertycollection/count/) { get; } | Ottiene il numero di elementi nella raccolta. |
| [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Restituisce un[`DocumentProperty`](../documentproperty/) oggetto per indice. |
| virtual [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Restituisce un[`DocumentProperty`](../documentproperty/) oggetto in base al nome della proprietà. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | Rimuove tutte le proprietà dalla raccolta. |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(*string*) | Restituisce`VERO` se nella raccolta esiste una proprietà con il nome specificato. |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | Restituisce un oggetto enumeratore che può essere utilizzato per scorrere tutti gli elementi nella raccolta. |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(*string*) | Ottiene l'indice di una proprietà in base al nome. |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(*string*) | Rimuove una proprietà con il nome specificato dalla raccolta. |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(*int*) | Rimuove una proprietà all'indice specificato. |

## Osservazioni

I nomi delle proprietà non fanno distinzione tra maiuscole e minuscole.

Le proprietà nella raccolta sono ordinate alfabeticamente in base al nome.

## Esempi

Mostra come lavorare con le proprietà personalizzate di un documento.

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

// Stampa tutte le proprietà personalizzate nel documento.
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

// Possiamo trovare queste proprietà personalizzate in Microsoft Word tramite "File" -> "Proprietà" > "Proprietà avanzate" > "Personalizzate".
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

// 3 - Svuota l'intera raccolta in una volta sola:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Guarda anche

* class [BuiltInDocumentProperties](../builtindocumentproperties/)
* class [CustomDocumentProperties](../customdocumentproperties/)
* class [DocumentProperty](../documentproperty/)
* spazio dei nomi [Aspose.Words.Properties](../../aspose.words.properties/)
* assemblea [Aspose.Words](../../)
