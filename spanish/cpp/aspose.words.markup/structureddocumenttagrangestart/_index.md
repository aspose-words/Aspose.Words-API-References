---
title: "Clase Aspose::Words::Markup::StructuredDocumentTagRangeStart"
linktitle: "StructuredDocumentTagRangeStart"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Markup::StructuredDocumentTagRangeStart. Representa el inicio de una etiqueta de documento estructurado con rango que acepta contenido de múltiples secciones. Consulte también StructuredDocumentTagRangeEnd. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class


Representa el inicio de una etiqueta de documento estructurado **ranged** que acepta contenido de múltiples secciones. Consulte también [StructuredDocumentTagRangeEnd](../structureddocumenttagrangeend/). Para obtener más información, visite el artículo de documentación [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class StructuredDocumentTagRangeStart : public Aspose::Words::Node,
                                        public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>,
                                        public Aspose::Words::Markup::IStructuredDocumentTag
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante. |
| [AppendChild](./appendchild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Agrega el nodo especificado al final del rango stdContent. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicado del nodo. |
| [get_Appearance](./get_appearance/)() override | Obtiene o establece la apariencia de la etiqueta de documento estructurado. |
| [get_Color](./get_color/)() override | Obtiene o establece el color de la etiqueta de documento estructurado. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Especifica un identificador de nodo personalizado. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Obtiene el documento al que pertenece este nodo. |
| [get_Id](./get_id/)() override | Especifica un Id numérico persistente, de solo lectura y único para esta etiqueta de documento estructurado. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Devuelve **true** si este nodo puede contener otros nodos. |
| [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() override | Especifica si el contenido de esta etiqueta de documento estructurado debe interpretarse como texto de marcador de posición (en contraposición al contenido de texto regular dentro de la etiqueta de documento estructurado). Si se establece en **true**, este estado se reanudará (mostrando el texto de marcador de posición) al abrir este documento. |
| [get_LastChild](./get_lastchild/)() | Obtiene el último hijo en el rango stdContent. |
| [get_Level](./get_level/)() const override | Obtiene el nivel en el que ocurre el inicio del rango de esta etiqueta de documento estructurado en el árbol del documento. |
| [get_LockContentControl](./get_lockcontentcontrol/)() override | Cuando se establece en **true**, esta propiedad prohibirá que un usuario elimine esta etiqueta de documento estructurado. |
| [get_LockContents](./get_lockcontents/)() override | Cuando se establece en **true**, esta propiedad prohibirá que un usuario edite el contenido de esta etiqueta de documento estructurado. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Obtiene el nodo que sigue inmediatamente a este nodo. |
| [get_NodeType](./get_nodetype/)() const override | Devuelve [StructuredDocumentTagRangeStart](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Obtiene el padre inmediato de este nodo. |
| [get_Placeholder](./get_placeholder/)() override | Obtiene el [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) que contiene texto de marcador de posición que debe mostrarse cuando el contenido de ejecución de esta etiqueta de documento estructurado está vacío, el elemento XML asignado asociado está vacío según lo especificado mediante el elemento [XmlMapping](./get_xmlmapping/) o el elemento [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) es **true**. |
| [get_PlaceholderName](./get_placeholdername/)() override | Obtiene o establece el Nombre del [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) que contiene texto de marcador de posición. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Obtiene el nodo que precede inmediatamente a este nodo. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Devuelve un objeto [Range](../../aspose.words/range/) que representa la porción de un documento que está contenida en este nodo. |
| [get_RangeEnd](./get_rangeend/)() | Especifica el final del rango si el [StructuredDocumentTag](../structureddocumenttag/) es una etiqueta de documento estructurado con rango. De lo contrario, devuelve **null**. |
| [get_SdtType](./get_sdttype/)() override | Obtiene el tipo de esta etiqueta de documento estructurado. |
| [get_Tag](./get_tag/)() const override | Especifica una etiqueta asociada al nodo de la etiqueta de documento estructurado actual. No puede ser **null**. |
| [get_Title](./get_title/)() const override | Especifica el nombre descriptivo asociado a esta etiqueta de documento estructurado. No puede ser **null**. |
| [get_WordOpenXML](./get_wordopenxml/)() override | Obtiene una cadena que representa el XML contenido dentro del nodo en el formato [FlatOpc](../../aspose.words/saveformat/). |
| [get_WordOpenXMLMinimal](./get_wordopenxmlminimal/)() | Obtiene una cadena que representa el XML contenido dentro del nodo en formato [FlatOpc](../../aspose.words/saveformat/). A diferencia de la propiedad [WordOpenXML](./get_wordopenxml/), este método genera un documento simplificado que excluye cualquier parte no relacionada con el contenido. |
| [get_XmlMapping](./get_xmlmapping/)() override | Obtiene un objeto que representa el mapeo de este rango de etiqueta de documento estructurado a datos XML en una parte XML personalizada del documento actual. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Obtiene el primer ancestro del [NodeType](../../aspose.words/nodetype/) especificado. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) override | Devuelve una colección en vivo de nodos hijos que coinciden con los tipos especificados. |
| [GetEnumerator](./getenumerator/)() override | Proporciona soporte para la iteración al estilo foreach sobre los nodos hijos de este nodo. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo siguiente según el algoritmo de recorrido en preorden del árbol. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Un método de utilidad que convierte un valor de enumeración de tipo de nodo en una cadena legible para el usuario. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo anterior según el algoritmo de recorrido en preorden del árbol. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina a sí mismo del nodo padre. |
| [RemoveAllChildren](./removeallchildren/)() | Elimina todos los nodos entre este nodo de inicio de rango y el nodo de fin de rango. |
| [RemoveSelfOnly](./removeselfonly/)() override | Elimina este inicio de rango y los nodos de fin de rango apropiados de la etiqueta de documento estructurado, pero mantiene su contenido dentro del árbol del documento. |
| [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) override | Método set para [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance](./get_appearance/). |
| [set_Color](./set_color/)(System::Drawing::Color) override | Método set para [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Color](./get_color/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Método set para [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) override | Método set para [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/). |
| [set_LockContentControl](./set_lockcontentcontrol/)(bool) override | Método set para [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_LockContentControl](./get_lockcontentcontrol/). |
| [set_LockContents](./set_lockcontents/)(bool) override | Método setter para [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_LockContents](./get_lockcontents/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PlaceholderName](./set_placeholdername/)(System::String) override | Método setter para [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_PlaceholderName](./get_placeholdername/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Tag](./set_tag/)(System::String) override | Método setter para [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Tag](./get_tag/). |
| [set_Title](./set_title/)(System::String) override | Método setter para [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Title](./get_title/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](./settemplateweakptr/)(uint32_t) override |  |
| [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Markup::SdtType) | Inicializa una nueva instancia de la clase **Structured document tag range start**. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo obtener las propiedades de etiquetas de documento estructurado de varias secciones.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");

auto rangeStartTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, true)->idx_get(0));
auto rangeEndTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeEnd>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeEnd, true)->idx_get(0));

std::cout << "StructuredDocumentTagRangeStart values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeStartTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|Title: {0}", rangeStartTag->get_Title()) << std::endl;
std::cout << System::String::Format(u"\t|PlaceholderName: {0}", rangeStartTag->get_PlaceholderName()) << std::endl;
std::cout << System::String::Format(u"\t|IsShowingPlaceholderText: {0}", rangeStartTag->get_IsShowingPlaceholderText()) << std::endl;
std::cout << System::String::Format(u"\t|LockContentControl: {0}", rangeStartTag->get_LockContentControl()) << std::endl;
std::cout << System::String::Format(u"\t|LockContents: {0}", rangeStartTag->get_LockContents()) << std::endl;
std::cout << System::String::Format(u"\t|Level: {0}", rangeStartTag->get_Level()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeStartTag->get_NodeType()) << std::endl;
std::cout << System::String::Format(u"\t|RangeEnd: {0}", rangeStartTag->get_RangeEnd()) << std::endl;
std::cout << System::String::Format(u"\t|Color: {0}", rangeStartTag->get_Color().ToArgb()) << std::endl;
std::cout << System::String::Format(u"\t|SdtType: {0}", rangeStartTag->get_SdtType()) << std::endl;
std::cout << System::String::Format(u"\t|FlatOpcContent: {0}", rangeStartTag->get_WordOpenXML()) << std::endl;
std::cout << System::String::Format(u"\t|Tag: {0}\n", rangeStartTag->get_Tag()) << std::endl;

std::cout << "StructuredDocumentTagRangeEnd values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeEndTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeEndTag->get_NodeType()) << std::endl;
```

## Ver también

* Class [Node](../../aspose.words/node/)
* Interface [IStructuredDocumentTag](../istructureddocumenttag/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
