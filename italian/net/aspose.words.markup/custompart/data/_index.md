---
title: CustomPart.Data
second_title: Aspose.Words per .NET API Reference
description: CustomPart proprietà. Contiene i dati di questa parte personalizzata.
type: docs
weight: 30
url: /it/net/aspose.words.markup/custompart/data/
---
## CustomPart.Data property

Contiene i dati di questa parte personalizzata.

```csharp
public byte[] Data { get; set; }
```

### Osservazioni

Questa proprietà è applicabile solo quando[`IsExternal`](../isexternal/) è`falso`.

Il valore predefinito è una matrice di byte vuota. Il valore non può essere`nullo`.

### Esempi

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

// Possiamo rimuovere elementi da questa raccolta singolarmente o tutti in una volta.
doc.PackageCustomParts.RemoveAt(2);

Assert.AreEqual(2, doc.PackageCustomParts.Count);

doc.PackageCustomParts.Clear();

Assert.AreEqual(0, doc.PackageCustomParts.Count);
```

### Guarda anche

* class [CustomPart](../)
* spazio dei nomi [Aspose.Words.Markup](../../custompart/)
* assemblea [Aspose.Words](../../../)


