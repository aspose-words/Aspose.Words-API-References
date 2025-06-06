---
title: Document.PackageCustomParts
linktitle: PackageCustomParts
articleTitle: PackageCustomParts
second_title: Aspose.Words per .NET
description: Gestisci le parti personalizzate nel tuo pacchetto OOXML senza sforzo. Accedi e modifica i contenuti collegati con facilità, per una maggiore flessibilità e funzionalità dei documenti.
type: docs
weight: 320
url: /it/net/aspose.words/document/packagecustomparts/
---
## Document.PackageCustomParts property

Ottiene o imposta la raccolta di parti personalizzate (contenuto arbitrario) collegate al pacchetto OOXML tramite "relazioni sconosciute".

```csharp
public CustomPartCollection PackageCustomParts { get; set; }
```

## Osservazioni

Non confondere queste parti personalizzate con i dati XML personalizzati. Se devi accedere alle parti XML personalizzate, usa[`CustomXmlParts`](../customxmlparts/) proprietà.

Questa raccolta contiene parti OOXML il cui genitore è il pacchetto OOXML e i cui target sono di una "relazione sconosciuta". Per ulteriori informazioni vedere[`CustomPart`](../../../aspose.words.markup/custompart/).

Aspose.Words carica e salva le parti personalizzate solo nei documenti OOXML.

Questa proprietà non può essere`null`.

## Esempi

Mostra come accedere alla raccolta di parti personalizzate arbitrarie di un documento.

```csharp
Document doc = new Document(MyDir + "Custom parts OOXML package.docx");

Assert.AreEqual(2, doc.PackageCustomParts.Count);

// Clona la seconda parte, quindi aggiungi il clone alla raccolta.
CustomPart clonedPart = doc.PackageCustomParts[1].Clone();
doc.PackageCustomParts.Add(clonedPart);
Assert.AreEqual(3, doc.PackageCustomParts.Count);

// Enumera la raccolta e stampa ogni parte.
using (IEnumerator<CustomPart> enumerator = doc.PackageCustomParts.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Part index {index}:");
        Console.WriteLine($"\tName:\t\t\t\t{enumerator.Current.Name}");
        Console.WriteLine($"\tContent type:\t\t{enumerator.Current.ContentType}");
        Console.WriteLine($"\tRelationship type:\t{enumerator.Current.RelationshipType}");
        Console.WriteLine(enumerator.Current.IsExternal ?
            "\tSourced from outside the document" :
            $"\tStored within the document, length: {enumerator.Current.Data.Length} bytes");
        index++;
    }
}

// Possiamo rimuovere gli elementi da questa raccolta singolarmente o tutti in una volta.
doc.PackageCustomParts.RemoveAt(2);

Assert.AreEqual(2, doc.PackageCustomParts.Count);

doc.PackageCustomParts.Clear();

Assert.AreEqual(0, doc.PackageCustomParts.Count);
```

### Guarda anche

* class [CustomPartCollection](../../../aspose.words.markup/custompartcollection/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
