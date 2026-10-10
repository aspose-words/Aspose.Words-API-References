---
title: "Aspose::Words::Paragraph clase"
linktitle: "Paragraph"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Paragraph clase. Representa un párrafo de texto. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 47000
url: /es/cpp/aspose.words/paragraph/
---
## Paragraph class


Representa un párrafo de texto. Para obtener más información, visite el artículo de documentación [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/).

```cpp
class Paragraph : public Aspose::Words::CompositeNode,
                  public Aspose::Words::IParaAttrSource,
                  public Aspose::Words::IRunAttrSource,
                  public Aspose::Words::Revisions::ITrackableNode
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante para visitar el final del párrafo del documento. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante para visitar el inicio del párrafo del documento. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendField](./appendfield/)(Aspose::Words::Fields::FieldType, bool) | Añade un campo a este párrafo. |
| [AppendField](./appendfield/)(const System::String\&) | Añade un campo a este párrafo. |
| [AppendField](./appendfield/)(const System::String\&, const System::String\&) | Añade un campo a este párrafo. |
| [Clone](../node/clone/)(bool) | Crea un duplicado del nodo. |
| [get_BreakIsStyleSeparator](./get_breakisstyleseparator/)() | Verdadero si este salto de párrafo es un Separador de [Style](../style/). Un separador de estilo permite que un párrafo conste de partes que tienen diferentes estilos de párrafo. |
| [get_Count](../compositenode/get_count/)() | Obtiene el número de hijos inmediatos de este nodo. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Especifica un identificador de nodo personalizado. |
| virtual [get_Document](../node/get_document/)() const | Obtiene el documento al que pertenece este nodo. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Obtiene el primer hijo del nodo. |
| [get_FrameFormat](./get_frameformat/)() | Proporciona acceso a las propiedades de formato del marco. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Devuelve **true** si este nodo tiene algún nodo hijo. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Devuelve **true** ya que este nodo puede tener nodos hijos. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Devuelve true si este objeto fue eliminado en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsEndOfCell](./get_isendofcell/)() | Verdadero si este párrafo es el último párrafo en una [Cell](../../aspose.words.tables/cell/); falso en caso contrario. |
| [get_IsEndOfDocument](./get_isendofdocument/)() | Verdadero si este párrafo es el último párrafo en la última sección del documento. |
| [get_IsEndOfHeaderFooter](./get_isendofheaderfooter/)() | Verdadero si este párrafo es el último párrafo en el [HeaderFooter](../headerfooter/) (historia principal de texto) de una [Section](../section/); falso en caso contrario. |
| [get_IsEndOfSection](./get_isendofsection/)() | Verdadero si este párrafo es el último párrafo en el [Body](../body/) (historia principal de texto) de una [Section](../section/); falso en caso contrario. |
| [get_IsFormatRevision](./get_isformatrevision/)() | Devuelve true si el formato del objeto se modificó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsInCell](./get_isincell/)() | Verdadero si este párrafo es un hijo inmediato de [Cell](../../aspose.words.tables/cell/); falso en caso contrario. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Devuelve true si este objeto fue insertado en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsListItem](./get_islistitem/)() | Verdadero cuando el párrafo es un elemento en una lista con viñetas o numerada en la revisión original. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Devuelve **true** si este objeto fue movido (eliminado) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Devuelve **true** si este objeto fue movido (insertado) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Obtiene el último hijo del nodo. |
| [get_ListFormat](./get_listformat/)() | Proporciona acceso a las propiedades de formato de lista del párrafo. |
| [get_ListLabel](./get_listlabel/)() | Obtiene un objeto [ListLabel](./get_listlabel/) que brinda acceso al valor de numeración de la lista y al formato de este párrafo. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Obtiene el nodo que sigue inmediatamente a este nodo. |
| [get_NodeType](./get_nodetype/)() const override | Devuelve [Paragraph](../nodetype/). |
| [get_ParagraphBreakFont](./get_paragraphbreakfont/)() | Proporciona acceso al formato de fuente del carácter de salto de párrafo. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Proporciona acceso a las propiedades de formato del párrafo. |
| [get_ParentNode](../node/get_parentnode/)() | Obtiene el padre inmediato de este nodo. |
| [get_ParentSection](./get_parentsection/)() | Recupera la [Section](../section/) padre del párrafo. |
| [get_ParentStory](./get_parentstory/)() | Recupera la historia a nivel de sección principal que puede ser [Body](../body/) o [HeaderFooter](../headerfooter/). |
| [get_PreviousSibling](../node/get_previoussibling/)() | Obtiene el nodo que precede inmediatamente a este nodo. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Devuelve un objeto [Range](../range/) que representa la porción de un documento que está contenida en este nodo. |
| [get_Runs](./get_runs/)() | Proporciona acceso a la colección tipada de fragmentos de texto dentro del párrafo. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Obtiene el primer ancestro del [NodeType](../nodetype/) especificado. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Devuelve un nodo hijo N-ésimo que coincide con el tipo especificado. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Devuelve una colección en vivo de nodos hijos que coinciden con el tipo especificado. |
| [GetEffectiveTabStops](./geteffectivetabstops/)() | Devuelve una matriz de todas las tabulaciones aplicadas a este párrafo, incluidas las aplicadas indirectamente mediante estilos o listas. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Proporciona soporte para la iteración al estilo foreach sobre los nodos hijos de este nodo. |
| [GetText](./gettext/)() override | Obtiene el texto de este párrafo incluyendo el carácter de fin de párrafo. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Devuelve el índice del nodo hijo especificado en la matriz de nodos hijos. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertField](./insertfield/)(Aspose::Words::Fields::FieldType, bool, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Inserta un campo en este párrafo. |
| [InsertField](./insertfield/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Inserta un campo en este párrafo. |
| [InsertField](./insertfield/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Inserta un campo en este párrafo. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)() | Une ejecuciones con el mismo formato en el párrafo. |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)(const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\&) | Une ejecuciones con el mismo formato en el párrafo. |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo siguiente según el algoritmo de recorrido en preorden del árbol. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Un método de utilidad que convierte un valor de enumeración de tipo de nodo en una cadena legible para el usuario. |
| [Paragraph](./paragraph/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Inicializa una nueva instancia de la clase [Paragraph](./). |
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


[Paragraph](./) is a block-level node and can be a child of classes derived from [Story](../story/) or [InlineStory](../inlinestory/).

[Paragraph](./) can contain any number of inline-level nodes and bookmarks.

La lista completa de nodos secundarios que pueden aparecer dentro de un párrafo consta de [BookmarkStart](../bookmarkstart/), [BookmarkEnd](../bookmarkend/), [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/), [FormField](../../aspose.words.fields/formfield/), [Comment](../comment/), [Footnote](../../aspose.words.notes/footnote/), [Run](../run/), [SpecialChar](../specialchar/), [Shape](../../aspose.words.drawing/shape/), [GroupShape](../../aspose.words.drawing/groupshape/), [SmartTag](../../aspose.words.markup/smarttag/).

Un párrafo válido en Microsoft Word siempre termina con un carácter de salto de párrafo y un párrafo válido mínimo consiste únicamente en un salto de párrafo. La clase [Paragraph](./) agrega automáticamente el carácter de salto de párrafo apropiado al final y este carácter no forma parte de los nodos secundarios del [Paragraph](./), por lo tanto un [Paragraph](./) puede estar vacío.

No incluya los caracteres de fin de párrafo [ParagraphBreak](../controlchar/paragraphbreak/) o fin de celda [Cell](../controlchar/cell/) dentro del texto del párrafo, ya que podrían invalidar el párrafo cuando el documento se abra en Microsoft Word.

## Ejemplos



Muestra cómo construir un documento Aspose.Words manualmente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un documento en blanco contiene una sección, un cuerpo y un párrafo.
// Llame al método "RemoveAllChildren" para eliminar todos esos nodos,
// y termine con un nodo de documento sin hijos.
doc->RemoveAllChildren();

// Este documento ahora no tiene nodos hijos compuestos a los que podamos añadir contenido.
// Si deseamos editarlo, necesitaremos volver a poblar su colección de nodos.
// Primero, cree una nueva sección y luego añádala como hijo al nodo raíz del documento.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Establezca algunas propiedades de configuración de página para la sección.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Una sección necesita un cuerpo, que contendrá y mostrará todo su contenido
// en la página entre el encabezado y el pie de página de la sección.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Crea un párrafo, establece algunas propiedades de formato y luego añádelo como hijo al cuerpo.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Finalmente, agrega contenido al documento. Crea un run,
// establece su apariencia y contenido, y luego añádelo como hijo al párrafo.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## Ver también

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
