---
title: CustomPart.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words per .NET
description: Scopri come gestire i nomi CustomPart nei pacchetti OOXML. Imposta o recupera facilmente nomi assoluti per un'integrazione perfetta e funzionalità avanzate.
type: docs
weight: 50
url: /it/net/aspose.words.markup/custompart/name/
---
## CustomPart.Name property

Ottiene o imposta il nome assoluto di questa parte all'interno del pacchetto OOXML o dell'URL di destinazione.

```csharp
public string Name { get; set; }
```

## Osservazioni

Se la destinazione della relazione è interna, questa proprietà è il nome assoluto della parte all'interno del pacchetto. Se la destinazione della relazione è esterna, questa proprietà è l'URL di destinazione.

Il valore predefinito è una stringa vuota. Un valore valido deve essere una stringa non vuota.

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

* class [CustomPart](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
