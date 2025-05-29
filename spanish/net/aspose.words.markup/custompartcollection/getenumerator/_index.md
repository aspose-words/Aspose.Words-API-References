---
title: CustomPartCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words para .NET
description: Explora el método GetEnumerator de CustomPartCollection para iterar fácilmente todos los elementos de tu colección. ¡Optimiza la gestión de tus datos hoy mismo!
type: docs
weight: 70
url: /es/net/aspose.words.markup/custompartcollection/getenumerator/
---
## CustomPartCollection.GetEnumerator method

Devuelve un objeto enumerador que se puede utilizar para iterar sobre todos los elementos de la colección.

```csharp
public IEnumerator<CustomPart> GetEnumerator()
```

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

* class [CustomPart](../../custompart/)
* class [CustomPartCollection](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
