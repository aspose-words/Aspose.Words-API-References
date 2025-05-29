---
title: CustomPart.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words para .NET
description: Descubra cómo administrar los nombres de CustomPart en paquetes OOXML. Configure o recupere fácilmente nombres absolutos para una integración fluida y una funcionalidad mejorada.
type: docs
weight: 50
url: /es/net/aspose.words.markup/custompart/name/
---
## CustomPart.Name property

Obtiene o establece el nombre absoluto de esta parte dentro del paquete OOXML o la URL de destino.

```csharp
public string Name { get; set; }
```

## Observaciones

Si el objetivo de la relación es interno, entonces esta propiedad es el nombre de la parte absoluta dentro del paquete. Si el objetivo de la relación es externo, entonces esta propiedad es la URL de destino.

El valor predeterminado es una cadena vacía. Un valor válido debe ser una cadena que no esté vacía.

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
