---
title: DocumentBase
second_title: Referencia de API de Aspose.Words para .NET
description: Proporciona la clase base abstracta para un documento principal y un documento de glosario de un documento de Word.
type: docs
weight: 430
url: /es/net/aspose.words/documentbase/
---
## DocumentBase class

Proporciona la clase base abstracta para un documento principal y un documento de glosario de un documento de Word.

```csharp
public abstract class DocumentBase : CompositeNode
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape) { get; set; } | Obtiene o establece la forma de fondo del documento. Puede ser nulo. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Obtiene todos los nodos secundarios inmediatos de este nodo. |
| [Count](../../aspose.words/compositenode/count) { get; } | Obtiene el número de hijos inmediatos de este nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Especifica el identificador de nodo personalizado. |
| override [Document](../../aspose.words/documentbase/document) { get; } |  |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Obtiene el primer hijo del nodo. |
| [FontInfos](../../aspose.words/documentbase/fontinfos) { get; } | Proporciona acceso a las propiedades de las fuentes utilizadas en este documento. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Devuelve verdadero si este nodo tiene nodos secundarios. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Devuelve verdadero ya que este nodo puede tener nodos secundarios. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Obtiene el último hijo del nodo. |
| [Lists](../../aspose.words/documentbase/lists) { get; } | Proporciona acceso al formato de lista utilizado en el documento. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback) { get; set; } | Llamado cuando se inserta o elimina un nodo en el documento. |
| abstract [NodeType](../../aspose.words/node/nodetype) { get; } | Obtiene el tipo de este nodo. |
| [PageColor](../../aspose.words/documentbase/pagecolor) { get; set; } | Obtiene o establece el color de página del documento. Esta propiedad es una versión más simple de[`BackgroundShape`](./backgroundshape) . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Obtiene el padre inmediato de este nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range) { get; } | Devuelve un **Rango** objeto que representa la parte de un documento que está contenido en este nodo. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback) { get; set; } | Permite controlar cómo se cargan los recursos externos. |
| [Styles](../../aspose.words/documentbase/styles) { get; } | Devuelve una colección de estilos definidos en el documento. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback) { get; set; } | Llamado durante varios procedimientos de procesamiento de documentos cuando se detecta un problema que podría resultar en datos o pérdida de fidelidad de formato. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept)(DocumentVisitor) | Acepta un visitante. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Agrega el nodo especificado al final de la lista de nodos secundarios para este nodo. |
| [Clone](../../aspose.words/node/clone)(bool) | Crea un duplicado del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Reservado para uso del sistema. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Obtiene el primer ancestro del especificado[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Obtiene el primer ancestro del tipo de objeto especificado. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Devuelve un enésimo nodo secundario que coincide con el tipo especificado. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Devuelve una colección activa de nodos secundarios que coinciden con el tipo especificado. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Proporciona soporte para la iteración de cada estilo sobre los nodos secundarios de este nodo. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [ImportNode](../../aspose.words/documentbase/importnode#importnode)(Node, bool) | Importa un nodo de otro documento al documento actual. |
| [ImportNode](../../aspose.words/documentbase/importnode#importnode_1)(Node, bool, ImportFormatMode) | Importa un nodo de otro documento al documento actual con una opción para controlar el formato. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Devuelve el índice del nodo secundario especificado en la matriz de nodos secundarios. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Inserta el nodo especificado inmediatamente después del nodo de referencia especificado. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Inserta el nodo especificado inmediatamente antes del nodo de referencia especificado. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Obtiene el siguiente nodo de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Agrega el nodo especificado al principio de la lista de nodos secundarios para este nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Obtiene el nodo anterior de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [Remove](../../aspose.words/node/remove)() | Se elimina a sí mismo del padre. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Elimina todos los nodos secundarios del nodo actual. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Elimina el nodo secundario especificado. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Elimina todo[`SmartTag`](../../aspose.words.markup/smarttag) nodos descendientes del nodo actual. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Selecciona el primer nodo que coincide con la expresión XPath. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exporta el contenido del nodo a una cadena utilizando las opciones de guardado especificadas. |

### Observaciones

Aspose.Words representa un documento de Word como un árbol de nodos.[`DocumentBase`](../documentbase) es un nodo raíz del árbol que contiene todos los demás nodos del documento.

[`DocumentBase`](../documentbase) también almacena información de todo el documento, como[`Styles`](./styles) y [`Lists`](./lists) que los nodos del árbol podrían referirse.

### Ejemplos

Muestra cómo inicializar las subclases de DocumentBase.

```csharp
Document doc = new Document();

Assert.AreEqual(typeof(DocumentBase), doc.GetType().BaseType);

GlossaryDocument glossaryDoc = new GlossaryDocument();
doc.GlossaryDocument = glossaryDoc;

Assert.AreEqual(typeof(DocumentBase), glossaryDoc.GetType().BaseType);
```

### Ver también

* class [CompositeNode](../compositenode)
* espacio de nombres [Aspose.Words](../../aspose.words)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
