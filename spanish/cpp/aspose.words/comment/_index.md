---
title: "Clase Aspose::Words::Comment"
linktitle: "Comment"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Comment. Representa un contenedor para el texto de un comentario. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words/comment/
---
## Comment class


Representa un contenedor para el texto de un comentario. Para obtener más información, visite el artículo de documentación [Working with Comments](https://docs.aspose.com/words/cpp/working-with-comments/).

```cpp
class Comment : public Aspose::Words::InlineStory,
                public Aspose::Words::INodeWithAnnotationId,
                public Aspose::Words::Revisions::IMoveTrackableNode
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante para visitar el final del comentario. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante para visitar el inicio del comentario. |
| [AddReply](./addreply/)(const System::String\&, const System::String\&, System::DateTime, const System::String\&) | Agrega una respuesta a este comentario. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | Crea un duplicado del nodo. |
| [Comment](./comment/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Inicializa una nueva instancia de la clase [Comment](./). |
| [Comment](./comment/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&, const System::String\&, System::DateTime) | Inicializa una nueva instancia de la clase [Comment](./). |
| [EnsureMinimum](../inlinestory/ensureminimum/)() | Si el último hijo no es un párrafo, crea y agrega un párrafo vacío. |
| [get_Ancestor](./get_ancestor/)() | Devuelve el objeto [Comment](./) padre. Devuelve **null** para los comentarios de nivel superior. |
| [get_Author](./get_author/)() const | Obtiene o establece el nombre del autor de un comentario. |
| [get_Count](../compositenode/get_count/)() | Obtiene el número de hijos inmediatos de este nodo. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Especifica un identificador de nodo personalizado. |
| [get_DateTime](./get_datetime/)() const | Obtiene la fecha y hora en que se realizó el comentario. |
| [get_DateTimeUtc](./get_datetimeutc/)() | Obtiene la fecha y hora UTC en que se realizó el comentario. |
| virtual [get_Document](../node/get_document/)() const | Obtiene el documento al que pertenece este nodo. |
| [get_Done](./get_done/)() const | Obtiene o establece la bandera que indica que el comentario ha sido marcado como completado. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Obtiene el primer hijo del nodo. |
| [get_FirstParagraph](../inlinestory/get_firstparagraph/)() override | Obtiene el primer párrafo de la historia. |
| [get_Font](../inlinestory/get_font/)() | Proporciona acceso al formato de fuente del carácter ancla de este objeto. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Devuelve **true** si este nodo tiene algún nodo hijo. |
| [get_Id](./get_id/)() const | Obtiene o establece el identificador del comentario. |
| [get_Initial](./get_initial/)() const | Obtiene o establece las iniciales del usuario asociado a un comentario específico. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Devuelve **true** ya que este nodo puede tener nodos hijos. |
| [get_IsDeleteRevision](../inlinestory/get_isdeleterevision/)() | Devuelve true si este objeto fue eliminado en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsInsertRevision](../inlinestory/get_isinsertrevision/)() | Devuelve true si este objeto fue insertado en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsMoveFromRevision](../inlinestory/get_ismovefromrevision/)() | Devuelve **true** si este objeto fue movido (eliminado) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsMoveToRevision](../inlinestory/get_ismovetorevision/)() | Devuelve **true** si este objeto fue movido (insertado) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Obtiene el último hijo del nodo. |
| [get_LastParagraph](../inlinestory/get_lastparagraph/)() override | Obtiene el último párrafo de la historia. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Obtiene el nodo que sigue inmediatamente a este nodo. |
| [get_NodeType](./get_nodetype/)() const override | Devuelve [Comment](../nodetype/). |
| [get_Paragraphs](../inlinestory/get_paragraphs/)() override | Obtiene una colección de párrafos que son hijos inmediatos de la historia. |
| [get_ParentId](./get_parentid/)() const | Obtiene el ID del comentario padre. Un valor de **%-1** significa que el comentario no tiene padre. |
| [get_ParentNode](../node/get_parentnode/)() | Obtiene el padre inmediato de este nodo. |
| [get_ParentParagraph](../inlinestory/get_parentparagraph/)() | Recupera el [Paragraph](../paragraph/) padre de este nodo. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Obtiene el nodo que precede inmediatamente a este nodo. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Devuelve un objeto [Range](../range/) que representa la porción de un documento que está contenida en este nodo. |
| [get_Replies](./get_replies/)() | Devuelve una colección de objetos [Comment](./) que son hijos inmediatos del comentario especificado. |
| [get_StoryType](./get_storytype/)() override | Devuelve [Comments](../storytype/). |
| [get_Tables](../inlinestory/get_tables/)() override | Obtiene una colección de tablas que son hijos inmediatos de la historia. |
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
| [RemoveAllReplies](./removeallreplies/)() | Elimina todas las respuestas a este comentario. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveReply](./removereply/)(const System::SharedPtr\<Aspose::Words::Comment\>\&) | Elimina la respuesta especificada a este comentario. |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Elimina todos los nodos descendientes de [SmartTag](../../aspose.words.markup/smarttag/) del nodo actual. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Selecciona el primer [Node](../node/) que coincide con la expresión XPath. |
| [set_Author](./set_author/)(const System::String\&) | Método setter para [Aspose::Words::Comment::get_Author](./get_author/). |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Método setter para [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_DateTime](./set_datetime/)(System::DateTime) | Obtiene la fecha y hora en que se realizó el comentario. |
| [set_Done](./set_done/)(bool) | Método setter para [Aspose::Words::Comment::get_Done](./get_done/). |
| [set_Id](./set_id/)(int32_t) | Método setter para [Aspose::Words::Comment::get_Id](./get_id/). |
| [set_Initial](./set_initial/)(const System::String\&) | Método setter para [Aspose::Words::Comment::get_Initial](./get_initial/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ParentId](./set_parentid/)(int32_t) | Establece el ID del comentario padre. Un valor de **%-1** significa que el comentario no tiene padre. |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SetText](./settext/)(const System::String\&) | Este es un método de conveniencia que permite establecer fácilmente el texto del comentario. |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |
| static [Type](./type/)() |  |
## Observaciones


Un comentario es una anotación que está anclada a una región de texto o a una posición en el texto. Un comentario puede contener una cantidad arbitraria de contenido a nivel de bloque.

Si un objeto [Comment](./) aparece por sí solo, el comentario está anclado a la posición del objeto [Comment](./).

Para anclar un comentario a una región de texto se requieren tres objetos: [Comment](./), [CommentRangeStart](../commentrangestart/) y [CommentRangeEnd](../commentrangeend/). Los tres objetos deben compartir el mismo valor de [Id](./get_id/).

[Comment](./) is an inline-level node and can only be a child of [Paragraph](../paragraph/).

[Comment](./) can contain [Paragraph](../paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.

## Ejemplos



Muestra cómo agregar un comentario a un documento y luego responder a él.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

// Coloque el comentario en un nodo del cuerpo del documento.
// Este comentario aparecerá en la ubicación de su párrafo,
// fuera del margen derecho de la página, y con una línea punteada que lo conecta a su párrafo.
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Agregue una respuesta, que aparecerá bajo su comentario padre.
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");

// Los comentarios y las respuestas son ambos nodos Comment.
ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Comment, true)->get_Count());

// Los comentarios que no responden a otros comentarios son "de nivel superior". No tienen comentarios ancestros.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_Ancestor()));

// Las respuestas tienen un comentario ancestro de nivel superior.
ASPOSE_ASSERT_EQ(comment, comment->get_Replies()->idx_get(0)->get_Ancestor());

doc->Save(get_ArtifactsDir() + u"Comment.AddCommentWithReply.docx");
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

* Class [InlineStory](../inlinestory/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
