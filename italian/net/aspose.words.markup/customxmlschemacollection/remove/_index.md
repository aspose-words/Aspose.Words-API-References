---
title: CustomXmlSchemaCollection.Remove
second_title: Aspose.Words per .NET API Reference
description: CustomXmlSchemaCollection metodo. Rimuove il valore specificato dalla raccolta.
type: docs
weight: 80
url: /it/net/aspose.words.markup/customxmlschemacollection/remove/
---
## CustomXmlSchemaCollection.Remove method

Rimuove il valore specificato dalla raccolta.

```csharp
public void Remove(string name)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | String | Il valore con distinzione tra maiuscole e minuscole da rimuovere. |

### Esempi

Mostra come lavorare con una raccolta di schemi XML.

```csharp
Document doc = new Document();

string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello, World!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

// Aggiunge un'associazione allo schema XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Clona la raccolta di associazioni di schemi XML della parte XML personalizzata,
// e poi aggiungi un paio di nuovi schemi al clone.
CustomXmlSchemaCollection schemas = xmlPart.Schemas.Clone();
schemas.Add("http://www.w3.org/2001/XMLSchema-istanza");
schemas.Add("http://schemas.microsoft.com/office/2006/metadata/contentType");

Assert.AreEqual(3, schemas.Count);
Assert.AreEqual(2, schemas.IndexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Enumera gli schemi e stampa ogni elemento.
using (IEnumerator<string> enumerator = schemas.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine(enumerator.Current);
}

// Di seguito sono riportati tre modi per rimuovere gli schemi dalla raccolta.
// 1 - Rimuovi uno schema per indice:
schemas.RemoveAt(2);

// 2 - Rimuovi uno schema per valore:
schemas.Remove("http://www.w3.org/2001/XMLSchema");

// 3 - Utilizza il metodo "Clear" per svuotare immediatamente la raccolta.
schemas.Clear();

Assert.AreEqual(0, schemas.Count);
```

### Guarda anche

* class [CustomXmlSchemaCollection](../)
* spazio dei nomi [Aspose.Words.Markup](../../customxmlschemacollection/)
* assemblea [Aspose.Words](../../../)


