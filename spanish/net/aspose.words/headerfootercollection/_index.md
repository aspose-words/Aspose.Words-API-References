---
title: Class HeaderFooterCollection
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.HeaderFooterCollection clase. Proporciona acceso escrito aHeaderFooter nodos de un Sección .
type: docs
weight: 2930
url: /es/net/aspose.words/headerfootercollection/
---
## HeaderFooterCollection class

Proporciona acceso escrito a[`HeaderFooter`](../headerfooter/) nodos de un **Sección** .

```csharp
public class HeaderFooterCollection : NodeCollection
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Obtiene el número de nodos de la colección. |
| [Item](../../aspose.words/headerfootercollection/item/) { get; } | Recupera un **EncabezadoPie de página** en el índice dado. (3 indexers) |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | Agrega un nodo al final de la colección. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Elimina todos los nodos de esta colección y del documento. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | Determina si un nodo está en la colección. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Proporciona una iteración de estilo "foreach" simple sobre la colección de nodos. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | Devuelve el índice de base cero del nodo especificado. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | Inserta un nodo en la colección en el índice especificado. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious_1)(bool) | Vincula o desvincula todos los encabezados y pies de página a los correspondientes encabezados y pies de página en la sección anterior. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious)(HeaderFooterType, bool) | Vincula o desvincula el encabezado o pie de página especificado con el correspondiente encabezado o pie de página de la sección anterior. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | Elimina el nodo de la colección y del documento. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | Elimina el nodo en el índice especificado de la colección y del documento. |
| [ToArray](../../aspose.words/headerfootercollection/toarray/#toarray)() | Copia todo`EncabezadoPie de página` s de la colección a una nueva matriz de`EncabezadoPie de página` s. (2 methods) |

### Observaciones

Puede haber un máximo de uno **EncabezadoPie de página**

de cada[`HeaderFooterType`](../headerfootertype/) por  **Sección** .

**EncabezadoPie de página** los objetos pueden ocurrir en cualquier orden en la colección.

### Ejemplos

Muestra cómo eliminar todos los pies de página de un documento.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Iterar a través de cada sección y eliminar pies de página de todo tipo.
foreach (Section section in doc.OfType<Section>())
{
    // Hay tres tipos de tipos de encabezado y pie de página.
    // 1 - El encabezado/pie de página "Primero", que solo aparece en la primera página de una sección.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - El encabezado/pie de página "Principal", que aparece en las páginas impares.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

      // 3 - El encabezado/pie de página "Even", que aparece en las páginas pares.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

Muestra cómo crear un encabezado y un pie de página.

```csharp
Document doc = new Document();

// Crear un encabezado y agregarle un párrafo. El texto de ese párrafo
// aparecerá en la parte superior de cada página de esta sección, encima del texto del cuerpo principal.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Crea un pie de página y añádele un párrafo. El texto de ese párrafo
// aparecerá en la parte inferior de cada página de esta sección, debajo del texto del cuerpo principal.
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.False(footer.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

Assert.AreEqual(footer, para.ParentStory);
Assert.AreEqual(footer.ParentSection, para.ParentSection);
Assert.AreEqual(footer.ParentSection, header.ParentSection);

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### Ver también

* class [NodeCollection](../nodecollection/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)


