---
title: CustomPartCollection Class
linktitle: CustomPartCollection
articleTitle: CustomPartCollection
second_title: Aspose.Words per .NET
description: Esplora la classe Aspose.Words.Markup.CustomPartCollection per gestire in modo efficiente gli oggetti CustomPart. Migliora subito le tue capacità di elaborazione dei documenti!
type: docs
weight: 4600
url: /it/net/aspose.words.markup/custompartcollection/
---
## CustomPartCollection class

Rappresenta una raccolta di[`CustomPart`](../custompart/) oggetti.

Per saperne di più, visita il[Tag di documenti strutturati o controllo dei contenuti](https://docs.aspose.com/words/net/working-with-content-control-sdt/) articolo di documentazione.

```csharp
public class CustomPartCollection : IEnumerable<CustomPart>
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [CustomPartCollection](custompartcollection/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.markup/custompartcollection/count/) { get; } | Ottiene il numero di elementi contenuti nella raccolta. |
| [Item](../../aspose.words.markup/custompartcollection/item/) { get; set; } | Ottiene o imposta un elemento all'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words.markup/custompartcollection/add/)(*[CustomPart](../custompart/)*) | Aggiunge un elemento alla collezione. |
| [Clear](../../aspose.words.markup/custompartcollection/clear/)() | Rimuove tutti gli elementi dalla raccolta. |
| [Clone](../../aspose.words.markup/custompartcollection/clone/)() | Crea una copia completa di questa raccolta e dei suoi elementi. |
| [GetEnumerator](../../aspose.words.markup/custompartcollection/getenumerator/)() | Restituisce un oggetto enumeratore che può essere utilizzato per scorrere tutti gli elementi nella raccolta. |
| [RemoveAt](../../aspose.words.markup/custompartcollection/removeat/)(*int*) | Rimuove un elemento all'indice specificato. |

## Osservazioni

Normalmente non è necessario creare istanze di questa classe. È possibile accedere alle parti personalizzate relative al pacchetto OOXML tramite[`PackageCustomParts`](../../aspose.words/document/packagecustomparts/) proprietà.

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

* class [CustomPart](../custompart/)
* spazio dei nomi [Aspose.Words.Markup](../../aspose.words.markup/)
* assemblea [Aspose.Words](../../)
