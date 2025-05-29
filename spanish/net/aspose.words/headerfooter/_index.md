---
title: HeaderFooter Class
linktitle: HeaderFooter
articleTitle: HeaderFooter
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.HeaderFooter, su solución para gestionar encabezados y pies de sección sin esfuerzo. ¡Mejore el formato de sus documentos hoy mismo!
type: docs
weight: 3530
url: /es/net/aspose.words/headerfooter/
---
## HeaderFooter class

Representa un contenedor para el texto del encabezado o pie de página de una sección.

Para obtener más información, visite el[Trabajar con encabezados y pies de página](https://docs.aspose.com/words/net/working-with-headers-and-footers/) Artículo de documentación.

```csharp
public class HeaderFooter : Story
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [HeaderFooter](headerfooter/)(*[DocumentBase](../documentbase/), [HeaderFooterType](../headerfootertype/)*) | Crea un nuevo encabezado o pie de página del tipo especificado. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtiene el número de hijos inmediatos de este nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica un identificador de nodo personalizado. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtiene el primer hijo del nodo. |
| [FirstParagraph](../../aspose.words/story/firstparagraph/) { get; } | Obtiene el primer párrafo de la historia. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Devuelve`verdadero` si este nodo tiene nodos secundarios. |
| [HeaderFooterType](../../aspose.words/headerfooter/headerfootertype/) { get; } | Obtiene el tipo de este encabezado/pie de página. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Devuelve`verdadero` ya que este nodo puede tener nodos secundarios. |
| [IsHeader](../../aspose.words/headerfooter/isheader/) { get; } | Verdadero si esto`HeaderFooter` El objeto es un encabezado. |
| [IsLinkedToPrevious](../../aspose.words/headerfooter/islinkedtoprevious/) { get; set; } | Verdadero si este encabezado o pie de página está vinculado al encabezado o pie de página correspondiente en la sección anterior. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtiene el último hijo del nodo. |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | Obtiene el último párrafo de la historia. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo inmediatamente siguiente a este nodo. |
| override [NodeType](../../aspose.words/headerfooter/nodetype/) { get; } | DevuelveHeaderFooter . |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | Obtiene una colección de párrafos que son hijos inmediatos de la historia. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [ParentSection](../../aspose.words/headerfooter/parentsection/) { get; } | Obtiene la sección principal de esta historia. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un[`Range`](../range/)objeto que representa la porción de un documento que está contenida en este nodo. |
| [StoryType](../../aspose.words/story/storytype/) { get; } | Obtiene el tipo de esta historia. |
| [Tables](../../aspose.words/story/tables/) { get; } | Obtiene una colección de tablas que son hijas inmediatas de la historia. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words/headerfooter/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Acepta un visitante. |
| override [AcceptEnd](../../aspose.words/headerfooter/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Acepta un visitante por visitar el final del encabezado. |
| override [AcceptStart](../../aspose.words/headerfooter/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Acepta un visitante por visitar el inicio del encabezado. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Agrega el nodo especificado al final de la lista de nodos secundarios para este nodo. |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(*string*) | Un método de acceso directo que crea un[`Paragraph`](../paragraph/) objeto con texto opcional y lo agrega al final de este objeto. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicado del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navegador que puede utilizarse para recorrer y leer nodos. |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | Elimina todas las formas del texto de esta historia. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Obtiene el primer ancestro del especificado[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtiene el primer ancestro del tipo de objeto especificado. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Devuelve un nodo secundario N que coincide con el tipo especificado. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Devuelve una colección activa de nodos secundarios que coinciden con el tipo especificado. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Proporciona soporte para cada iteración de estilo sobre los nodos secundarios de este nodo. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Devuelve el índice del nodo secundario especificado en la matriz de nodos secundarios. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Inserta el nodo especificado inmediatamente después del nodo de referencia especificado. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Inserta el nodo especificado inmediatamente antes del nodo de referencia especificado. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Obtiene el siguiente nodo según el algoritmo de recorrido del árbol de preorden. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Agrega el nodo especificado al comienzo de la lista de nodos secundarios para este nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Obtiene el nodo anterior según el algoritmo de recorrido del árbol de preorden. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina a sí mismo del padre. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Elimina todos los nodos secundarios del nodo actual. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Elimina el nodo secundario especificado. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Elimina todo[`SmartTag`](../../aspose.words.markup/smarttag/) nodos descendientes del nodo actual. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Selecciona el primer[`Node`](../node/) que coincide con la expresión XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exporta el contenido del nodo en una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporta el contenido del nodo en una cadena utilizando las opciones de guardado especificadas. |

## Observaciones

`HeaderFooter` puede contener[`Paragraph`](../paragraph/) y[`Mesa`](../../aspose.words.tables/table/) nodos secundarios.

`HeaderFooter` es un nodo de nivel de sección y solo puede ser un hijo de[`Section`](../section/) . Solo puede haber uno`HeaderFooter` de cada uno[`HeaderFooterType`](./headerfootertype/) en un[`Section`](../section/).

Si[`Section`](../section/) no tiene una`HeaderFooter` de un tipo específico o el`HeaderFooter` no tiene nodos secundarios, este encabezado/pie de página se considera vinculado a el encabezado/pie de página del mismo tipo de la sección anterior en Microsoft Word.

Cuando`HeaderFooter` contiene al menos uno[`Paragraph`](../paragraph/), ya no se considera vinculado al anterior en Microsoft Word.

## Ejemplos

Muestra cómo reemplazar texto en el pie de página de un documento.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

Muestra cómo eliminar todos los pies de página de un documento.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Iterar a través de cada sección y eliminar pies de página de todo tipo.
foreach (Section section in doc.OfType<Section>())
{
    // Hay tres tipos de pie de página y encabezado.
    // 1 - El encabezado/pie de página "Primero", que solo aparece en la primera página de una sección.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - El encabezado/pie de página "Principal", que aparece en las páginas impares.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - El encabezado/pie de página "Par", que aparece en las páginas pares.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

Muestra cómo crear un encabezado y un pie de página.

```csharp
Document doc = new Document();

// Crea un encabezado y añade un párrafo. El texto de ese párrafo
// aparecerá en la parte superior de cada página de esta sección, encima del texto del cuerpo principal.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Crea un pie de página y añade un párrafo. El texto de ese párrafo
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

* class [Story](../story/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
