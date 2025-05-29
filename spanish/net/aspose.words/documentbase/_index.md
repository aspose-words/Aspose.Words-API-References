---
title: DocumentBase Class
linktitle: DocumentBase
articleTitle: DocumentBase
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.DocumentBase, la base esencial para crear y administrar documentos y glosarios de Word con facilidad y eficiencia.
type: docs
weight: 650
url: /es/net/aspose.words/documentbase/
---
## DocumentBase class

Proporciona la clase base abstracta para un documento principal y un documento de glosario de un documento de Word.

Para obtener más información, visite el[Modelo de objetos de documento (DOM) de Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Artículo de documentación.

```csharp
public abstract class DocumentBase : CompositeNode
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Obtiene o establece la forma del fondo del documento. Puede ser`nulo` . |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtiene el número de hijos inmediatos de este nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica un identificador de nodo personalizado. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | Obtiene esta instancia. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtiene el primer hijo del nodo. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Proporciona acceso a las propiedades de las fuentes utilizadas en este documento. |
| [FootnoteSeparators](../../aspose.words/documentbase/footnoteseparators/) { get; } | Proporciona acceso a los separadores de notas al pie/notas finales definidos en el documento. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Devuelve`verdadero` si este nodo tiene nodos secundarios. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Devuelve`verdadero` ya que este nodo puede tener nodos secundarios. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtiene el último hijo del nodo. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Proporciona acceso al formato de lista utilizado en el documento. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo inmediatamente siguiente a este nodo. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Se llama cuando se inserta o elimina un nodo en el documento. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Obtiene el tipo de este nodo. |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Obtiene o establece el color de página del documento. Esta propiedad es una versión más simple de[`BackgroundShape`](./backgroundshape/) . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un[`Range`](../range/)objeto que representa la porción de un documento que está contenida en este nodo. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Permite controlar cómo se cargan los recursos externos. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Devuelve una colección de estilos definidos en el documento. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Se llama durante varios procedimientos de procesamiento de documentos cuando se detecta un problema que podría resultar en pérdida de fidelidad de datos o formato. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Acepta un visitante. |
| abstract [AcceptEnd](../../aspose.words/compositenode/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Cuando se implementa en una clase derivada, llama al método VisitXXXEnd del visitante del documento especificado. |
| abstract [AcceptStart](../../aspose.words/compositenode/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Cuando se implementa en una clase derivada, llama al método VisitXXXStart del visitante del documento especificado. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Agrega el nodo especificado al final de la lista de nodos secundarios para este nodo. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicado del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navegador que puede utilizarse para recorrer y leer nodos. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Obtiene el primer ancestro del especificado[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtiene el primer ancestro del tipo de objeto especificado. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Devuelve un nodo secundario N que coincide con el tipo especificado. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Devuelve una colección activa de nodos secundarios que coinciden con el tipo especificado. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Proporciona soporte para cada iteración de estilo sobre los nodos secundarios de este nodo. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [ImportNode](../../aspose.words/documentbase/importnode/#importnode)(*[Node](../node/), bool*) | Importa un nodo de otro documento al documento actual. |
| [ImportNode](../../aspose.words/documentbase/importnode/#importnode_1)(*[Node](../node/), bool, [ImportFormatMode](../importformatmode/)*) | Importa un nodo de otro documento al documento actual con una opción para controlar el formato. |
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

Aspose.Words representa un documento de Word como un árbol de nodos.`DocumentBase` es un nodo raíz del árbol que contiene todos los demás nodos del documento.

`DocumentBase` También almacena información de todo el documento, como[`Styles`](./styles/) y [`Lists`](./lists/) a los que podrían hacer referencia los nodos del árbol.

## Ejemplos

Muestra cómo inicializar las subclases de DocumentBase.

```csharp
Document doc = new Document();

Assert.AreEqual(typeof(DocumentBase), doc.GetType().BaseType);

GlossaryDocument glossaryDoc = new GlossaryDocument();
doc.GlossaryDocument = glossaryDoc;

Assert.AreEqual(typeof(DocumentBase), glossaryDoc.GetType().BaseType);
```

### Ver también

* class [CompositeNode](../compositenode/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
