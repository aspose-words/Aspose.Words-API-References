---
title: "Aspose::Words::Markup::IStructuredDocumentTag interfaz"
linktitle: "IStructuredDocumentTag"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag interfaz. Interfaz para definir datos comunes para StructuredDocumentTag y StructuredDocumentTagRangeStart en C++."
type: docs
weight: 16000
url: /es/cpp/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface


Interfaz para definir datos comunes para [StructuredDocumentTag](../structureddocumenttag/) y [StructuredDocumentTagRangeStart](../structureddocumenttagrangestart/).

```cpp
class IStructuredDocumentTag : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| virtual [get_Appearance](./get_appearance/)() | Obtiene o establece la apariencia de la etiqueta de documento estructurado. |
| virtual [get_Color](./get_color/)() | Obtiene o establece el color de la etiqueta de documento estructurado. |
| virtual [get_Id](./get_id/)() | Especifica un Id numérico persistente de solo lectura único para este **SDT**. |
| virtual [get_IsMultiSection](./get_ismultisection/)() | Devuelve true si esta instancia es una etiqueta de documento estructurado con rango (multi sección). |
| virtual [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() | Especifica si el contenido de este **SDT** debe interpretarse como texto de marcador de posición (en lugar de contenido de texto regular dentro del **SDT**). Si se establece en true, este estado se reanudará (mostrando el texto de marcador de posición) al abrir este documento. |
| virtual [get_Level](./get_level/)() const | Obtiene el nivel en el que este **SDT** ocurre en el árbol del documento. |
| virtual [get_LockContentControl](./get_lockcontentcontrol/)() | Cuando se establece en true, esta propiedad prohibirá que un usuario elimine este **SDT**. |
| virtual [get_LockContents](./get_lockcontents/)() | Cuando se establece en true, esta propiedad prohibirá que un usuario edite el contenido de este **SDT**. |
| virtual [get_Node](./get_node/)() | Devuelve el objeto [Node](../../aspose.words/node/) que implementa esta interfaz. |
| virtual [get_Placeholder](./get_placeholder/)() | Obtiene el [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) que contiene texto de marcador de posición que debe mostrarse cuando el contenido de ejecución de este SDT está vacío, el elemento XML asignado asociado está vacío según lo especificado mediante el elemento [XmlMapping](./get_xmlmapping/) o el elemento [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) es true. |
| virtual [get_PlaceholderName](./get_placeholdername/)() | Obtiene o establece el Nombre del [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) que contiene texto de marcador de posición. |
| virtual [get_SdtType](./get_sdttype/)() | Obtiene el tipo de esta **Structured document tag**. |
| virtual [get_Tag](./get_tag/)() const | Especifica una etiqueta asociada al nodo SDT actual. No puede ser null. |
| virtual [get_Title](./get_title/)() const | Especifica el nombre descriptivo asociado a este **SDT**. No puede ser null. |
| virtual [get_WordOpenXML](./get_wordopenxml/)() | Obtiene una cadena que representa el XML contenido dentro del nodo en el formato [FlatOpc](../../aspose.words/saveformat/). |
| virtual [get_XmlMapping](./get_xmlmapping/)() | Obtiene un objeto que representa el mapeo de esta etiqueta de documento estructurado a datos XML en una parte XML personalizada del documento actual. |
| virtual [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) | Devuelve una colección en vivo de nodos hijos que coinciden con los tipos especificados. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [RemoveSelfOnly](./removeselfonly/)() | Elimina únicamente este nodo SDT, pero conserva su contenido dentro del árbol del documento. |
| virtual [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) | Método set para [Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance](./get_appearance/). |
| virtual [set_Color](./set_color/)(System::Drawing::Color) | Método set para [Aspose::Words::Markup::IStructuredDocumentTag::get_Color](./get_color/). |
| virtual [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) | Método set para [Aspose::Words::Markup::IStructuredDocumentTag::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/). |
| virtual [set_LockContentControl](./set_lockcontentcontrol/)(bool) | Método set para [Aspose::Words::Markup::IStructuredDocumentTag::get_LockContentControl](./get_lockcontentcontrol/). |
| virtual [set_LockContents](./set_lockcontents/)(bool) | Método set para [Aspose::Words::Markup::IStructuredDocumentTag::get_LockContents](./get_lockcontents/). |
| virtual [set_PlaceholderName](./set_placeholdername/)(System::String) | Método set para [Aspose::Words::Markup::IStructuredDocumentTag::get_PlaceholderName](./get_placeholdername/). |
| virtual [set_Tag](./set_tag/)(System::String) | Método set para [Aspose::Words::Markup::IStructuredDocumentTag::get_Tag](./get_tag/). |
| virtual [set_Title](./set_title/)(System::String) | Establecedor para [Aspose::Words::Markup::IStructuredDocumentTag::get_Title](./get_title/). |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo eliminar la etiqueta de documento estructurado, pero mantiene el contenido interno.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// Esta colección proporciona una interfaz unificada para acceder a etiquetas estructuradas con rango y sin rango.
System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>> sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(5, sdts->LINQ_Count());

// Aquí podemos obtener nodos hijos desde la interfaz común de etiquetas estructuradas con rango y sin rango.
for (auto&& sdt : System::IterateOver(sdts))
{
    if (sdt->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count() > 0)
    {
        sdt->RemoveSelfOnly();
    }
}

sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(0, sdts->LINQ_Count());
```

## Ver también

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
