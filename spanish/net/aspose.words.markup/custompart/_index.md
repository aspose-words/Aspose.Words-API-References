---
title: CustomPart Class
linktitle: CustomPart
articleTitle: CustomPart
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Markup.CustomPart para una gestión flexible de contenido. ¡Cree fácilmente piezas únicas y no estándar que superan la norma ISO/IEC 29500!
type: docs
weight: 4590
url: /es/net/aspose.words.markup/custompart/
---
## CustomPart class

Representa una parte personalizada (contenido arbitrario), que no está definida por el estándar ISO/IEC 29500.

Para obtener más información, visite el[Etiquetas de documentos estructurados o control de contenido](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Artículo de documentación.

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
| [IsExternal](../../aspose.words.markup/custompart/isexternal/) { get; set; } | Falso si esta parte personalizada se almacena dentro del paquete OOXML. Verdadero si esta parte personalizada es un destino externo. |
| [Name](../../aspose.words.markup/custompart/name/) { get; set; } | Obtiene o establece el nombre absoluto de esta parte dentro del paquete OOXML o la URL de destino. |
| [RelationshipType](../../aspose.words.markup/custompart/relationshiptype/) { get; set; } | Obtiene o establece el tipo de relación de la parte principal a esta parte personalizada. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Clone](../../aspose.words.markup/custompart/clone/)() | Realiza una copia "suficientemente profunda" del objeto. No duplica los bytes del objeto.[`Data`](./data/) valor. |

## Observaciones

Esta clase representa una parte OOXML que es un objetivo de una "relación desconocida". Todas las relaciones no definidas dentro de ISO/IEC 29500 se consideran "relaciones desconocidas". Las relaciones desconocidas están permitidas dentro de un documento Office Open XML siempre que se ajusten a las pautas de marcado de relaciones.

Microsoft Word conserva las partes personalizadas al abrir y guardar. Puede encontrar información adicional aquí: http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

Aspose.Words también realiza viajes de ida y vuelta a partes personalizadas y, además, permite acceder mediante programación a dichas partes a través de`CustomPart` y[`CustomPartCollection`](../custompartcollection/) objetos.

No confunda las piezas personalizadas con los datos XML personalizados. Utilice[`CustomXmlPart`](../customxmlpart/) Si necesita para acceder a datos XML personalizados.

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

* espacio de nombres [Aspose.Words.Markup](../../aspose.words.markup/)
* asamblea [Aspose.Words](../../)
