---
title: Class OfficeMath
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Math.OfficeMath clase. Representa un objeto de Office Math como función ecuación matriz o similar. Puede contener elementos secundarios  incluidas tiradas de texto matemático marcadores comentarios otrosOfficeMath instancias y algunos otros nodos.
type: docs
weight: 3880
url: /es/net/aspose.words.math/officemath/
---
## OfficeMath class

Representa un objeto de Office Math como función, ecuación, matriz o similar. Puede contener elementos secundarios , incluidas tiradas de texto matemático, marcadores, comentarios, otros`OfficeMath` instancias y algunos otros nodos.

```csharp
public class OfficeMath : CompositeNode
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Obtiene todos los nodos secundarios inmediatos de este nodo. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtiene el número de hijos inmediatos de este nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica el identificador de nodo personalizado. |
| [DisplayType](../../aspose.words.math/officemath/displaytype/) { get; set; } | Obtiene/establece el tipo de formato de visualización de Office Math que representa si una ecuación se muestra en línea con el texto o se muestra en su propia línea. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [EquationXmlEncoding](../../aspose.words.math/officemath/equationxmlencoding/) { get; set; } | Obtiene/establece una codificación que se usó para codificar la ecuación XML, si este objeto matemático de Office se lee desde ecuación XML. Usamos la codificación al guardar un documento para escribir en la misma codificación que se leyó. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtiene el primer hijo del nodo. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Devuelve verdadero si este nodo tiene nodos secundarios. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Devuelve verdadero ya que este nodo puede tener nodos secundarios. |
| [Justification](../../aspose.words.math/officemath/justification/) { get; set; } | Obtiene/establece la justificación matemática de Office. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtiene el último hijo del nodo. |
| [MathObjectType](../../aspose.words.math/officemath/mathobjecttype/) { get; } | Obtiene el tipo[`MathObjectType`](./mathobjecttype/) de este objeto Office Math. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words.math/officemath/nodetype/) { get; } | Devoluciones **NodeType.OfficeMath** . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [ParentParagraph](../../aspose.words.math/officemath/parentparagraph/) { get; } | Recupera el padre[`Paragraph`](../../aspose.words/paragraph/) de este nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un **Rango** objeto que representa la parte de un documento que está contenido en este nodo. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words.math/officemath/accept/)(DocumentVisitor) | Acepta un visitante. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Agrega el nodo especificado al final de la lista de nodos secundarios para este nodo. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicado del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Reservado para uso del sistema. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtiene el primer ancestro del especificado[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtiene el primer ancestro del tipo de objeto especificado. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Devuelve un enésimo nodo secundario que coincide con el tipo especificado. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Devuelve una colección activa de nodos secundarios que coinciden con el tipo especificado. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Proporciona soporte para la iteración de cada estilo sobre los nodos secundarios de este nodo. |
| [GetMathRenderer](../../aspose.words.math/officemath/getmathrenderer/)() | Crea y devuelve un objeto que se puede usar para convertir esta ecuación en una imagen. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Devuelve el índice del nodo secundario especificado en la matriz de nodos secundarios. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Inserta el nodo especificado inmediatamente después del nodo de referencia especificado. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Inserta el nodo especificado inmediatamente antes del nodo de referencia especificado. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtiene el siguiente nodo de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Agrega el nodo especificado al principio de la lista de nodos secundarios para este nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtiene el nodo anterior de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina a sí mismo del padre. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Elimina todos los nodos secundarios del nodo actual. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Elimina el nodo secundario especificado. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Elimina todo[`SmartTag`](../../aspose.words.markup/smarttag/) nodos descendientes del nodo actual. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Selecciona el primer nodo que coincide con la expresión XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporta el contenido del nodo a una cadena utilizando las opciones de guardado especificadas. |

### Observaciones

En esta versión de Aspose.Words,`OfficeMath` los nodos no proporcionan métodos públicos ni propiedades para crear o modificar un objeto OfficeMath. En esta versión no puedes instanciar Math nodos o modificar los existentes excepto eliminarlos.

`OfficeMath` solo puede ser hijo de[`Paragraph`](../../aspose.words/paragraph/).

### Ejemplos

Muestra cómo configurar el formato de visualización de Office Math.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// Los nodos de OfficeMath que son hijos de otros nodos de OfficeMath siempre están en línea.
// El nodo con el que estamos trabajando es el nodo base para cambiar su ubicación y tipo de visualización.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// Los formatos OOXML y WML utilizan la propiedad "EquationXmlEncoding".
Assert.IsNull(officeMath.EquationXmlEncoding);

// Cambiar la ubicación y el tipo de visualización del nodo OfficeMath.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Ver también

* class [CompositeNode](../../aspose.words/compositenode/)
* espacio de nombres [Aspose.Words.Math](../../aspose.words.math/)
* asamblea [Aspose.Words](../../)


