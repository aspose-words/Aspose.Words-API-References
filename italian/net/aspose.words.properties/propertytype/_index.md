---
title: PropertyType Enum
linktitle: PropertyType
articleTitle: PropertyType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.PropertyType per definire facilmente i tipi di dati delle proprietà dei documenti, per una migliore gestione e personalizzazione dei documenti.
type: docs
weight: 5230
url: /it/net/aspose.words.properties/propertytype/
---
## PropertyType enumeration

Specifica il tipo di dati di una proprietà del documento.

```csharp
public enum PropertyType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Boolean | `0` | La proprietà è un valore booleano. |
| DateTime | `1` | La proprietà è un valore di data e ora. |
| Double | `2` | La proprietà è un numero mobile. |
| Number | `3` | La proprietà è un numero intero. |
| String | `4` | La proprietà è un valore stringa. |
| StringArray | `5` | La proprietà è un array di stringhe. |
| ObjectArray | `6` | La proprietà è un array di oggetti. |
| ByteArray | `7` | La proprietà è un array di byte. |
| Other | `8` | La proprietà è di un altro tipo. |

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

* class [DocumentProperty](../documentproperty/)
* property [Type](../documentproperty/type/)
* spazio dei nomi [Aspose.Words.Properties](../../aspose.words.properties/)
* assemblea [Aspose.Words](../../)
