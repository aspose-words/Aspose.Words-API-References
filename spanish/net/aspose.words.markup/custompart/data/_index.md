---
title: CustomPart.Data
linktitle: Data
articleTitle: Data
second_title: Aspose.Words para .NET
description: Explora los datos de CustomPart. Accede a información detallada sobre tus piezas personalizadas para mejorar la precisión y la eficiencia de tus proyectos.
type: docs
weight: 30
url: /es/net/aspose.words.markup/custompart/data/
---
## CustomPart.Data property

Contiene los datos de esta pieza personalizada.

```csharp
public byte[] Data { get; set; }
```

## Observaciones

Esta propiedad es aplicable únicamente cuando[`IsExternal`](../isexternal/) es`FALSO`.

El valor predeterminado es una matriz de bytes vacía. El valor no puede ser`nulo`.

## Ejemplos

Muestra cómo acceder a la colección de partes personalizadas arbitrarias de un documento.

```csharp
Document doc = new Document(MyDir + "Custom parts OOXML package.docx");

Assert.AreEqual(2, doc.PackageCustomParts.Count);

// Clona la segunda parte y luego agrega el clon a la colección.
CustomPart clonedPart = doc.PackageCustomParts[1].Clone();
doc.PackageCustomParts.Add(clonedPart);
Assert.AreEqual(3, doc.PackageCustomParts.Count);

// Enumerar la colección e imprimir cada parte.
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

//Podemos eliminar elementos de esta colección individualmente o todos a la vez.
doc.PackageCustomParts.RemoveAt(2);

Assert.AreEqual(2, doc.PackageCustomParts.Count);

doc.PackageCustomParts.Clear();

Assert.AreEqual(0, doc.PackageCustomParts.Count);
```

### Ver también

* class [CustomPart](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
