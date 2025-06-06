---
title: SectionCollection Class
linktitle: SectionCollection
articleTitle: SectionCollection
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.SectionCollection su solución ideal para administrar secciones de documentos de manera eficiente con funciones potentes y flexibilidad.
type: docs
weight: 6570
url: /es/net/aspose.words/sectioncollection/
---
## SectionCollection class

Una colección de[`Section`](../section/) objetos en el documento.

Para obtener más información, visite el[Trabajar con secciones](https://docs.aspose.com/words/net/working-with-sections/) Artículo de documentación.

```csharp
public class SectionCollection : NodeCollection
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Obtiene el número de nodos en la colección. |
| [Item](../../aspose.words/sectioncollection/item/) { get; } | Recupera una sección en el índice dado. (2 indexers) |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Agrega un nodo al final de la colección. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Elimina todos los nodos de esta colección y del documento. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Determina si un nodo está en la colección. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Proporciona una iteración simple al estilo "foreach" sobre la colección de nodos. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Devuelve el índice basado en cero del nodo especificado. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Inserta un nodo en la colección en el índice especificado. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Elimina el nodo de la colección y del documento. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Elimina el nodo en el índice especificado de la colección y del documento. |
| [ToArray](../../aspose.words/sectioncollection/toarray/#toarray_1)() | Copia todas las secciones de la colección a una nueva matriz de secciones. (2 methods) |

## Observaciones

Un documento de Microsoft Word puede contener varias secciones. Para crear una sección en un documento de Microsoft Word, seleccione el comando Insertar/Salto y seleccione un tipo de salto. El salto especifica si la sección comienza en una página nueva o en la misma.

La inserción y eliminación de secciones mediante programación permite personalizar documentos producidos durante la combinación de correspondencia. Si un documento necesita tener contenido diferente o partes de él según ciertos criterios, puede crear un documento "maestro" que contenga varias secciones y eliminar algunas de ellas antes o después de la combinación de correspondencia.

## Ejemplos

Muestra cómo agregar y eliminar secciones en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

//Eliminar la primera sección del documento.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// Añade una copia de lo que ahora es la primera sección al final del documento.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

### Ver también

* class [NodeCollection](../nodecollection/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
