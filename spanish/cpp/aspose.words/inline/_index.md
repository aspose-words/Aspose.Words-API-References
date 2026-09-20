---
title: "Aspose::Words::Inline clase"
linktitle: "En línea"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Inline clase. Clase base para nodos de nivel en línea que pueden tener formato de carácter asociado, pero no pueden tener nodos hijos propios. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 36000
url: /es/cpp/aspose.words/inline/
---
## Inline class


Clase base para nodos de nivel en línea que pueden tener formato de carácter asociado, pero no pueden tener nodos hijos propios. Para obtener más información, visite el artículo de documentación [Logical Levels of Nodes in a Document](https://docs.aspose.com/words/cpp/logical-levels-of-nodes-in-a-document/).

```cpp
class Inline : public Aspose::Words::Node,
               public Aspose::Words::IInline,
               public Aspose::Words::Revisions::ITrackableNode
```

## Métodos

| Método | Descripción |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Acepta un visitante. |
| [Clone](../node/clone/)(bool) | Crea un duplicado del nodo. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Especifica un identificador de nodo personalizado. |
| virtual [get_Document](../node/get_document/)() const | Obtiene el documento al que pertenece este nodo. |
| [get_Font](./get_font/)() | Proporciona acceso al formato de fuente de este objeto. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Devuelve **true** si este nodo puede contener otros nodos. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Devuelve true si este objeto fue eliminado en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsFormatRevision](./get_isformatrevision/)() | Devuelve true si el formato del objeto se modificó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Devuelve true si este objeto fue insertado en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Devuelve **true** si este objeto fue movido (eliminado) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Devuelve **true** si este objeto fue movido (insertado) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Obtiene el nodo que sigue inmediatamente a este nodo. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Obtiene el tipo de este nodo. |
| [get_ParentNode](../node/get_parentnode/)() | Obtiene el padre inmediato de este nodo. |
| [get_ParentParagraph](./get_parentparagraph/)() | Recupera el [Paragraph](../paragraph/) padre de este nodo. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Obtiene el nodo que precede inmediatamente a este nodo. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Devuelve un objeto [Range](../range/) que representa la porción de un documento que está contenida en este nodo. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Obtiene el primer ancestro del [NodeType](../nodetype/) especificado. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| virtual [GetText](../node/gettext/)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo siguiente según el algoritmo de recorrido en preorden del árbol. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Un método de utilidad que convierte un valor de enumeración de tipo de nodo en una cadena legible para el usuario. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo anterior según el algoritmo de recorrido en preorden del árbol. |
| [Remove](../node/remove/)() | Se elimina a sí mismo del nodo padre. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Método setter para [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |
| static [Type](./type/)() |  |
## Observaciones


Una clase derivada de [Inline](./) puede ser un hijo de [Paragraph](../paragraph/).

## Ejemplos



Muestra cómo determinar el tipo de revisión de un nodo en línea.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision runs.docx");

// Cuando editamos el documento mientras la opción "Track Changes" encontrada en Revisar -> Seguimiento,
// está activada en Microsoft Word, los cambios que aplicamos cuentan como revisiones.
// Al editar un documento usando Aspose.Words, podemos comenzar a rastrear revisiones mediante
// invocando el método "StartTrackRevisions" del documento y detener el seguimiento usando el método "StopTrackRevisions".
// Podemos aceptar las revisiones para asimilarlas al documento
// o rechazarlas para modificar efectivamente el cambio propuesto.
ASSERT_EQ(6, doc->get_Revisions()->get_Count());

// El nodo padre de una revisión es el Run al que la revisión se refiere. Un Run es un nodo Inline.
auto run = System::ExplicitCast<Aspose::Words::Run>(doc->get_Revisions()->idx_get(0)->get_ParentNode());

System::SharedPtr<Aspose::Words::Paragraph> firstParagraph = run->get_ParentParagraph();
System::SharedPtr<Aspose::Words::RunCollection> runs = firstParagraph->get_Runs();

ASSERT_EQ(6, runs->ToArray()->get_Length());

// A continuación se presentan cinco tipos de revisiones que pueden marcar un nodo Inline.
// 1 -  Una revisión "insert".
// Esta revisión ocurre cuando insertamos texto mientras se rastrean los cambios.
ASSERT_TRUE(runs->idx_get(2)->get_IsInsertRevision());

// 2 -  Una revisión "format".
// Esta revisión ocurre cuando cambiamos el formato del texto mientras se rastrean los cambios.
ASSERT_TRUE(runs->idx_get(2)->get_IsFormatRevision());

// 3 -  Una revisión "move from".
// Cuando resaltamos texto en Microsoft Word y luego lo arrastramos a otro lugar del documento
// mientras se rastrean los cambios, aparecen dos revisiones.
// La revisión "move from" es una copia del texto original antes de moverlo.
ASSERT_TRUE(runs->idx_get(4)->get_IsMoveFromRevision());

// 4 -  Una revisión "move to".
// La revisión "move to" es el texto que movimos a su nueva posición en el documento.
// "Move from" y "move to" aparecen en pares para cada revisión de movimiento que realizamos.
// Aceptar una revisión de movimiento elimina la revisión "move from" y su texto,
// y conserva el texto de la revisión "move to".
// Rechazar una revisión de movimiento, por el contrario, conserva la revisión "move from" y elimina la revisión "move to".
ASSERT_TRUE(runs->idx_get(1)->get_IsMoveToRevision());

// 5 -  Una revisión "delete".
// Esta revisión ocurre cuando eliminamos texto mientras se rastrean los cambios. Cuando eliminamos texto de esta manera,
// permanecerá en el documento como una revisión hasta que aceptemos la revisión,
// lo que eliminará el texto de forma permanente, o rechacemos la revisión, lo que mantendrá el texto que eliminamos en su lugar.
ASSERT_TRUE(runs->idx_get(5)->get_IsDeleteRevision());
```

## Ver también

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
