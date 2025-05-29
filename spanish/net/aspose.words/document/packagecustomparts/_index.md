---
title: Document.PackageCustomParts
linktitle: PackageCustomParts
articleTitle: PackageCustomParts
second_title: Aspose.Words para .NET
description: Gestione fácilmente las partes personalizadas de su paquete OOXML. Acceda y modifique fácilmente el contenido vinculado para mejorar la flexibilidad y la funcionalidad de sus documentos.
type: docs
weight: 320
url: /es/net/aspose.words/document/packagecustomparts/
---
## Document.PackageCustomParts property

Obtiene o establece la colección de partes personalizadas (contenido arbitrario) que están vinculadas al paquete OOXML mediante "relaciones desconocidas".

```csharp
public CustomPartCollection PackageCustomParts { get; set; }
```

## Observaciones

No confunda estas partes personalizadas con datos XML personalizados. Si necesita acceder a partes XML personalizadas, utilice el[`CustomXmlParts`](../customxmlparts/) propiedad.

Esta colección contiene partes OOXML cuyo padre es el paquete OOXML y sus destinos son de una "relación desconocida". Para obtener más información, consulte[`CustomPart`](../../../aspose.words.markup/custompart/).

Aspose.Words carga y guarda partes personalizadas solo en documentos OOXML.

Esta propiedad no puede ser`nulo`.

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

* class [CustomPartCollection](../../../aspose.words.markup/custompartcollection/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
