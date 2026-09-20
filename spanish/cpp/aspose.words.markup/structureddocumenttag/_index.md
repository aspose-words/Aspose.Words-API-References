---
title: "Clase Aspose::Words::Markup::StructuredDocumentTag"
linktitle: "StructuredDocumentTag"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Markup::StructuredDocumentTag. Representa una etiqueta de documento estructurado (SDT o control de contenido) en un documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class


Representa una etiqueta de documento estructurado (SDT o control de contenido) en un documento. Para obtener más información, visite el artículo de documentación [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class StructuredDocumentTag : public Aspose::Words::CompositeNode,
                              public Aspose::Words::Markup::IMarkupNode,
                              public Aspose::Words::Revisions::ITrackableNode,
                              public Aspose::Words::IRunAttrSource,
                              public Aspose::Words::Markup::IStructuredDocumentTag
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante para visitar el final del [StructuredDocumentTag](./). |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante para visitar el inicio del [StructuredDocumentTag](./). |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clear](./clear/)() | Borra el contenido de esta etiqueta de documento estructurado y muestra un marcador de posición si está definido. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicado del nodo. |
| [get_Appearance](./get_appearance/)() override | Obtiene/establece la apariencia de una etiqueta de documento estructurado. |
| [get_BuildingBlockCategory](./get_buildingblockcategory/)() | Especifica la categoría del bloque de construcción para este nodo **SDT**. No puede ser **null**. |
| [get_BuildingBlockGallery](./get_buildingblockgallery/)() | Especifica el tipo de bloque de construcción para este **SDT**. No puede ser **null**. |
| [get_CalendarType](./get_calendartype/)() | Especifica el tipo de calendario para este **SDT**. El valor predeterminado es [Default](../sdtcalendartype/) |
| [get_Checked](./get_checked/)() | Obtiene/establece el estado actual del Checkbox **SDT**. El valor predeterminado de esta propiedad es **false**. |
| [get_Color](./get_color/)() override | Obtiene o establece el color de la etiqueta de documento estructurado. |
| [get_ContentsFont](./get_contentsfont/)() | Formato de [Font](../../aspose.words/font/) que se aplicará al texto ingresado en **SDT**. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Obtiene el número de hijos inmediatos de este nodo. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Especifica un identificador de nodo personalizado. |
| [get_DateDisplayFormat](./get_datedisplayformat/)() | Cadena que representa el formato en el que se muestran las fechas. |
| [get_DateDisplayLocale](./get_datedisplaylocale/)() | Permite establecer/obtener el formato de idioma para la fecha mostrada en este **SDT**. |
| [get_DateStorageFormat](./get_datestorageformat/)() | Obtiene/establece el formato en el que se almacena la fecha para un SDT de fecha cuando el **SDT** está vinculado a un nodo XML en el almacén de datos del documento. El valor predeterminado es [DateTime](../sdtdatestorageformat/) |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Obtiene el documento al que pertenece este nodo. |
| [get_EndCharacterFont](./get_endcharacterfont/)() | Formato de [Font](../../aspose.words/font/) que se aplicará al último carácter del texto ingresado en **SDT**. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Obtiene el primer hijo del nodo. |
| [get_FullDate](./get_fulldate/)() | Especifica la fecha y hora completas ingresadas por última vez en este **SDT**. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Devuelve **true** si este nodo tiene algún nodo hijo. |
| [get_Id](./get_id/)() override | Especifica un Id numérico persistente de solo lectura único para este **SDT**. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Devuelve **true** ya que este nodo puede tener nodos hijos. |
| [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() override | Especifica si el contenido de este **SDT** debe interpretarse como texto de marcador de posición (en lugar de contenido de texto regular dentro del SDT). Si se establece en **true**, este estado se reanudará (mostrando el texto de marcador de posición) al abrir este documento. |
| [get_IsTemporary](./get_istemporary/)() const | Especifica si este **SDT** debe eliminarse del documento WordProcessingML cuando su contenido se modifica. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Obtiene el último hijo del nodo. |
| [get_Level](./get_level/)() const override | Obtiene el nivel en el que este **SDT** ocurre en el árbol del documento. |
| [get_ListItems](./get_listitems/)() | Obtiene [SdtListItemCollection](../sdtlistitemcollection/) asociado con este **SDT**. |
| [get_LockContentControl](./get_lockcontentcontrol/)() override | Cuando se establece en **true**, esta propiedad prohibirá que un usuario elimine este **SDT**. |
| [get_LockContents](./get_lockcontents/)() override | Cuando se establece en **true**, esta propiedad prohibirá que un usuario edite el contenido de este **SDT**. |
| [get_Multiline](./get_multiline/)() | Especifica si este **SDT** permite varias líneas de texto. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Obtiene el nodo que sigue inmediatamente a este nodo. |
| [get_NodeType](./get_nodetype/)() const override | Devuelve [StructuredDocumentTag](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Obtiene el padre inmediato de este nodo. |
| [get_Placeholder](./get_placeholder/)() override | Obtiene el [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) que contiene el texto de marcador de posición que debe mostrarse cuando el contenido de ejecución de este SDT está vacío, el elemento XML asignado asociado está vacío según lo especificado mediante el elemento [XmlMapping](./get_xmlmapping/) o el elemento [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) es **true**. |
| [get_PlaceholderName](./get_placeholdername/)() override | Obtiene o establece el Nombre del [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) que contiene texto de marcador de posición. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Obtiene el nodo que precede inmediatamente a este nodo. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Devuelve un objeto [Range](../../aspose.words/range/) que representa la porción de un documento que está contenida en este nodo. |
| [get_SdtType](./get_sdttype/)() override | Obtiene el tipo de esta **Structured document tag**. |
| [get_Style](./get_style/)() | Obtiene o establece el [Style](../../aspose.words/style/) de la etiqueta de documento estructurado. |
| [get_StyleName](./get_stylename/)() | Obtiene o establece el nombre del estilo aplicado a la etiqueta de documento estructurado. |
| [get_Tag](./get_tag/)() const override | Especifica una etiqueta asociada al nodo SDT actual. No puede ser **null**. |
| [get_Title](./get_title/)() const override | Especifica el nombre descriptivo asociado a este **SDT**. No puede ser **null**. |
| [get_WordOpenXML](./get_wordopenxml/)() override | Obtiene una cadena que representa el XML contenido dentro del nodo en el formato [FlatOpc](../../aspose.words/saveformat/). |
| [get_WordOpenXMLMinimal](./get_wordopenxmlminimal/)() | Obtiene una cadena que representa el XML contenido dentro del nodo en formato [FlatOpc](../../aspose.words/saveformat/). A diferencia de la propiedad [WordOpenXML](./get_wordopenxml/), este método genera un documento simplificado que excluye cualquier parte no relacionada con el contenido. |
| [get_XmlMapping](./get_xmlmapping/)() override | Obtiene un objeto que representa el mapeo de esta etiqueta de documento estructurado a datos XML en una parte XML personalizada del documento actual. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Obtiene el primer ancestro del [NodeType](../../aspose.words/nodetype/) especificado. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Devuelve un nodo hijo N-ésimo que coincide con el tipo especificado. |
| [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) override | Devuelve una colección en vivo de nodos hijos que coinciden con el tipo especificado. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Proporciona soporte para la iteración al estilo foreach sobre los nodos hijos de este nodo. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Obtiene el texto de este nodo y de todos sus hijos. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Devuelve el índice del nodo hijo especificado en la matriz de nodos hijos. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo siguiente según el algoritmo de recorrido en preorden del árbol. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Un método de utilidad que convierte un valor de enumeración de tipo de nodo en una cadena legible para el usuario. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo anterior según el algoritmo de recorrido en preorden del árbol. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina a sí mismo del nodo padre. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Elimina todos los nodos hijos del nodo actual. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSelfOnly](./removeselfonly/)() override | Elimina únicamente este nodo SDT, pero conserva su contenido dentro del árbol del documento. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Elimina todos los nodos descendientes [SmartTag](../smarttag/) del nodo actual. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Selecciona el primer [Node](../../aspose.words/node/) que coincide con la expresión XPath. |
| [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) override | Método set para [Aspose::Words::Markup::StructuredDocumentTag::get_Appearance](./get_appearance/). |
| [set_BuildingBlockCategory](./set_buildingblockcategory/)(const System::String\&) | Método set para [Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory](./get_buildingblockcategory/). |
| [set_BuildingBlockGallery](./set_buildingblockgallery/)(const System::String\&) | Método set para [Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery](./get_buildingblockgallery/). |
| [set_CalendarType](./set_calendartype/)(Aspose::Words::Markup::SdtCalendarType) | Método set para [Aspose::Words::Markup::StructuredDocumentTag::get_CalendarType](./get_calendartype/). |
| [set_Checked](./set_checked/)(bool) | Método set para [Aspose::Words::Markup::StructuredDocumentTag::get_Checked](./get_checked/). |
| [set_Color](./set_color/)(System::Drawing::Color) override | Método set para [Aspose::Words::Markup::StructuredDocumentTag::get_Color](./get_color/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Método set para [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DateDisplayFormat](./set_datedisplayformat/)(const System::String\&) | Método set para [Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayFormat](./get_datedisplayformat/). |
| [set_DateDisplayLocale](./set_datedisplaylocale/)(int32_t) | Método set para [Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayLocale](./get_datedisplaylocale/). |
| [set_DateStorageFormat](./set_datestorageformat/)(Aspose::Words::Markup::SdtDateStorageFormat) | Método set para [Aspose::Words::Markup::StructuredDocumentTag::get_DateStorageFormat](./get_datestorageformat/). |
| [set_FullDate](./set_fulldate/)(System::DateTime) | Método set para [Aspose::Words::Markup::StructuredDocumentTag::get_FullDate](./get_fulldate/). |
| [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) override | Método set para [Aspose::Words::Markup::StructuredDocumentTag::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/). |
| [set_IsTemporary](./set_istemporary/)(bool) | Método set para [Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary](./get_istemporary/). |
| [set_LockContentControl](./set_lockcontentcontrol/)(bool) override | Método set para [Aspose::Words::Markup::StructuredDocumentTag::get_LockContentControl](./get_lockcontentcontrol/). |
| [set_LockContents](./set_lockcontents/)(bool) override | Método set para [Aspose::Words::Markup::StructuredDocumentTag::get_LockContents](./get_lockcontents/). |
| [set_Multiline](./set_multiline/)(bool) | Método set para [Aspose::Words::Markup::StructuredDocumentTag::get_Multiline](./get_multiline/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PlaceholderName](./set_placeholdername/)(System::String) override | Método set para [Aspose::Words::Markup::StructuredDocumentTag::get_PlaceholderName](./get_placeholdername/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Establecedor de [Aspose::Words::Markup::StructuredDocumentTag::get_Style](./get_style/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Establecedor de [Aspose::Words::Markup::StructuredDocumentTag::get_StyleName](./get_stylename/). |
| [set_Tag](./set_tag/)(System::String) override | Establecedor de [Aspose::Words::Markup::StructuredDocumentTag::get_Tag](./get_tag/). |
| [set_Title](./set_title/)(System::String) override | Establecedor de [Aspose::Words::Markup::StructuredDocumentTag::get_Title](./get_title/). |
| [SetCheckedSymbol](./setcheckedsymbol/)(int32_t, const System::String\&) | Establece el símbolo usado para representar el estado marcado de un control de contenido de casilla de verificación. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SetUncheckedSymbol](./setuncheckedsymbol/)(int32_t, const System::String\&) | Establece el símbolo usado para representar el estado desmarcado de un control de contenido de casilla de verificación. |
| [StructuredDocumentTag](./structureddocumenttag/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Markup::SdtType, Aspose::Words::Markup::MarkupLevel) | Inicializa una nueva instancia de la clase **Structured document tag**. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |
| static [Type](./type/)() |  |
## Observaciones


Las etiquetas de documento estructurado (SDT) permiten incrustar semántica definida por el cliente, así como su comportamiento y apariencia, en un documento.

En esta versión Aspose.Words ofrece varios métodos y propiedades públicas para manipular el comportamiento y el contenido de [StructuredDocumentTag](./). El mapeo de nodos SDT a paquetes XML personalizados dentro de un documento puede realizarse usando la propiedad [XmlMapping](./get_xmlmapping/).

[StructuredDocumentTag](./) can occur in a document in the following places:

* Block-level - Among paragraphs and tables, as a child of a [Body](../../aspose.words/body/), [HeaderFooter](../../aspose.words/headerfooter/), [Comment](../../aspose.words/comment/), [Footnote](../../aspose.words.notes/footnote/) or a [Shape](../../aspose.words.drawing/shape/) node.
* Row-level - Among rows in a table, as a child of a [Table](../../aspose.words.tables/table/) node.
* Cell-level - Among cells in a table row, as a child of a [Row](../../aspose.words.tables/row/) node.
* Inline-level - Among inline content inside, as a child of a [Paragraph](../../aspose.words/paragraph/).
* Nested inside another [StructuredDocumentTag](./).



## Ejemplos



Muestra cómo trabajar con estilos para elementos de control de contenido.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A continuación se presentan dos formas de aplicar un estilo del documento a una etiqueta de documento estructurado.
// 1 -  Aplicar un objeto de estilo de la colección de estilos del documento:
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Referenciar un estilo en el documento por su nombre:
auto sdtRichText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RichText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtRichText->set_StyleName(u"Quote");

builder->InsertNode(sdtPlainText);
builder->InsertNode(sdtRichText);

ASSERT_EQ(Aspose::Words::NodeType::StructuredDocumentTag, sdtPlainText->get_NodeType());

System::SharedPtr<Aspose::Words::NodeCollection> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true);

for (auto&& node : System::IterateOver(tags))
{
    auto sdt = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(node);

    std::cout << sdt->get_WordOpenXMLMinimal() << std::endl;

    ASSERT_EQ(Aspose::Words::StyleIdentifier::Quote, sdt->get_Style()->get_StyleIdentifier());
    ASSERT_EQ(u"Quote", sdt->get_StyleName());
}
```

## Ver también

* Class [CompositeNode](../../aspose.words/compositenode/)
* Interface [IStructuredDocumentTag](../istructureddocumenttag/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
