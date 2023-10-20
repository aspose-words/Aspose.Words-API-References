---
title: CustomPart Class
linktitle: CustomPart
articleTitle: CustomPart
second_title: Aspose.Words para .NET
description: Aspose.Words.Markup.CustomPart clase. Representa una pieza personalizada contenido arbitrario que no está definida por el estándar ISO/IEC 29500 en C#.
type: docs
weight: 3900
url: /es/net/aspose.words.markup/custompart/
---
## CustomPart class

Representa una pieza personalizada (contenido arbitrario), que no está definida por el estándar ISO/IEC 29500.

Para obtener más información, visite el[Etiquetas de documentos estructurados o control de contenido](https://docs.aspose.com/words/net/working-with-content-control-sdt/) artículo de documentación.

```csharp
public class CustomPart
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [CustomPart](custompart/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [ContentType](../../aspose.words.markup/custompart/contenttype/) { get; set; } | Especifica el tipo de contenido de esta parte personalizada. |
| [Data](../../aspose.words.markup/custompart/data/) { get; set; } | Contiene los datos de esta pieza personalizada. |
| [IsExternal](../../aspose.words.markup/custompart/isexternal/) { get; set; } | Falso si esta parte personalizada está almacenada dentro del paquete OOXML. Verdadero si esta pieza personalizada es un destino externo. |
| [Name](../../aspose.words.markup/custompart/name/) { get; set; } | Obtiene o establece el nombre absoluto de esta parte dentro del paquete OOXML o la URL de destino. |
| [RelationshipType](../../aspose.words.markup/custompart/relationshiptype/) { get; set; } | Obtiene o establece el tipo de relación del artículo principal con este artículo personalizado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Clone](../../aspose.words.markup/custompart/clone/)() | Hace una copia "suficientemente profunda" del objeto. No duplica los bytes del[`Data`](./data/) valor. |

## Observaciones

Esta clase representa una parte OOXML que es el objetivo de una "relación desconocida". Todas las relaciones no definidas en ISO/IEC 29500 se consideran "relaciones desconocidas". Las relaciones desconocidas se permiten dentro de un documento Office Open XML siempre que cumplan con a las pautas de marcado de relaciones.

Microsoft Word conserva las partes personalizadas durante los ciclos de abrir/guardar. Puede encontrar información adicional aquí http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

Aspose.Words también recorre partes personalizadas y, además, permite acceder mediante programación a dichas partes a través del`CustomPart` y[`CustomPartCollection`](../custompartcollection/) objetos.

No confunda partes personalizadas con datos XML personalizados. Usar[`CustomXmlPart`](../customxmlpart/) si necesita para acceder a datos XML personalizados.

## Ejemplos

Muestra cómo acceder a la colección de piezas personalizadas arbitrarias de un documento.

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

// Podemos eliminar elementos de esta colección individualmente o todos a la vez.
doc.PackageCustomParts.RemoveAt(2);

Assert.AreEqual(2, doc.PackageCustomParts.Count);

doc.PackageCustomParts.Clear();

Assert.AreEqual(0, doc.PackageCustomParts.Count);
```

### Ver también

* espacio de nombres [Aspose.Words.Markup](../../aspose.words.markup/)
* asamblea [Aspose.Words](../../)
