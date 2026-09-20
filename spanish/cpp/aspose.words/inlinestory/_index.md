---
title: "Clase Aspose::Words::InlineStory"
linktitle: "InlineStory"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::InlineStory. Clase base para nodos de nivel en línea que pueden contener párrafos y tablas. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 37000
url: /es/cpp/aspose.words/inlinestory/
---
## InlineStory class


Clase base para nodos de nivel en línea que pueden contener párrafos y tablas. Para obtener más información, visite el artículo de documentación [Logical Levels of Nodes in a Document](https://docs.aspose.com/words/cpp/logical-levels-of-nodes-in-a-document/).

```cpp
class InlineStory : public Aspose::Words::CompositeNode,
                    public Aspose::Words::IInline,
                    public Aspose::Words::IStory
```

## Métodos

| Método | Descripción |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Acepta un visitante. |
| virtual [AcceptEnd](../compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Cuando se implementa en una clase derivada, llama al método VisitXXXEnd del visitante de documento especificado. |
| virtual [AcceptStart](../compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Cuando se implementa en una clase derivada, llama al método VisitXXXStart del visitante de documento especificado. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | Crea un duplicado del nodo. |
| [EnsureMinimum](./ensureminimum/)() | Si el último hijo no es un párrafo, crea y agrega un párrafo vacío. |
| [get_Count](../compositenode/get_count/)() | Obtiene el número de hijos inmediatos de este nodo. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Especifica un identificador de nodo personalizado. |
| virtual [get_Document](../node/get_document/)() const | Obtiene el documento al que pertenece este nodo. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Obtiene el primer hijo del nodo. |
| [get_FirstParagraph](./get_firstparagraph/)() override | Obtiene el primer párrafo de la historia. |
| [get_Font](./get_font/)() | Proporciona acceso al formato de fuente del carácter ancla de este objeto. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Devuelve **true** si este nodo tiene algún nodo hijo. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Devuelve **true** ya que este nodo puede tener nodos hijos. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Devuelve true si este objeto fue eliminado en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Devuelve true si este objeto fue insertado en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Devuelve **true** si este objeto fue movido (eliminado) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Devuelve **true** si este objeto fue movido (insertado) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Obtiene el último hijo del nodo. |
| [get_LastParagraph](./get_lastparagraph/)() override | Obtiene el último párrafo de la historia. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Obtiene el nodo que sigue inmediatamente a este nodo. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Obtiene el tipo de este nodo. |
| [get_Paragraphs](./get_paragraphs/)() override | Obtiene una colección de párrafos que son hijos inmediatos de la historia. |
| [get_ParentNode](../node/get_parentnode/)() | Obtiene el padre inmediato de este nodo. |
| [get_ParentParagraph](./get_parentparagraph/)() | Recupera el [Paragraph](../paragraph/) padre de este nodo. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Obtiene el nodo que precede inmediatamente a este nodo. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Devuelve un objeto [Range](../range/) que representa la porción de un documento que está contenida en este nodo. |
| virtual [get_StoryType](./get_storytype/)() | Devuelve el tipo de la historia. |
| [get_Tables](./get_tables/)() override | Obtiene una colección de tablas que son hijos inmediatos de la historia. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Obtiene el primer ancestro del [NodeType](../nodetype/) especificado. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Devuelve un nodo hijo N-ésimo que coincide con el tipo especificado. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Devuelve una colección en vivo de nodos hijos que coinciden con el tipo especificado. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Proporciona soporte para la iteración al estilo foreach sobre los nodos hijos de este nodo. |
| [GetText](../compositenode/gettext/)() override | Obtiene el texto de este nodo y de todos sus hijos. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Devuelve el índice del nodo hijo especificado en la matriz de nodos hijos. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo siguiente según el algoritmo de recorrido en preorden del árbol. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Un método de utilidad que convierte un valor de enumeración de tipo de nodo en una cadena legible para el usuario. |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo anterior según el algoritmo de recorrido en preorden del árbol. |
| [Remove](../node/remove/)() | Se elimina a sí mismo del nodo padre. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Elimina todos los nodos hijos del nodo actual. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Elimina todos los nodos descendientes de [SmartTag](../../aspose.words.markup/smarttag/) del nodo actual. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Selecciona el primer [Node](../node/) que coincide con la expresión XPath. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Método setter para [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |
| static [Type](./type/)() |  |
## Observaciones


[InlineStory](./) is a container for block-level nodes [Paragraph](../paragraph/) and [Table](../../aspose.words.tables/table/).

Las clases que derivan de [InlineStory](./) son nodos de nivel en línea que pueden contener su propio texto (párrafos y tablas). Por ejemplo, un nodo [Comment](../comment/) contiene el texto de un comentario y un [Footnote](../../aspose.words.notes/footnote/) contiene el texto de una nota al pie.

## Ejemplos



Muestra cómo insertar y personalizar notas al pie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Agregue texto y refiérelo con una nota al pie. Esta nota al pie colocará una pequeña referencia en superíndice
// después del texto al que hace referencia y creará una entrada debajo del texto principal al final de la página.
// Esta entrada contendrá la marca de referencia de la nota al pie y el texto de referencia,
// que pasaremos al método "InsertFootnote" del generador de documentos.
builder->Write(u"Main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// Si esta propiedad se establece en "true", entonces la marca de referencia de nuestra nota al pie
// será su índice entre todas las notas al pie de la sección.
// Esta es la primera nota al pie, por lo que la marca de referencia será "1".
ASSERT_TRUE(footnote->get_IsAuto());

// Podemos mover el generador de documentos dentro de la nota al pie para editar su texto de referencia.
builder->MoveTo(footnote->get_FirstParagraph());
builder->Write(u" More text added by a DocumentBuilder.");
builder->MoveToDocumentEnd();

ASSERT_EQ(u"\u0002 Footnote text. More text added by a DocumentBuilder.", footnote->GetText().Trim());

builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// Podemos establecer una marca de referencia personalizada que la nota al pie usará en lugar de su número de índice.
footnote->set_ReferenceMark(u"RefMark");

ASSERT_FALSE(footnote->get_IsAuto());

// Un marcador con la bandera "IsAuto" establecida en true aún mostrará su índice real
// incluso si los marcadores anteriores muestran marcas de referencia personalizadas, por lo que la marca de referencia de este marcador será "3".
builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

ASSERT_TRUE(footnote->get_IsAuto());

doc->Save(get_ArtifactsDir() + u"InlineStory.AddFootnote.docx");
```


Muestra cómo añadir un comentario a un párrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// En Microsoft Word, podemos hacer clic derecho en este comentario en el cuerpo del documento para editarlo o responderlo.
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## Ver también

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
