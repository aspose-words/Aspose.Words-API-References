---
title: "Interface Aspose::Words::Markup::IStructuredDocumentTag"
linktitle: "IStructuredDocumentTag"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Interface Aspose::Words::Markup::IStructuredDocumentTag. Interface permettant de définir des données communes pour StructuredDocumentTag et StructuredDocumentTagRangeStart en C++."
type: docs
weight: 16000
url: /fr/cpp/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface


Interface permettant de définir des données communes pour [StructuredDocumentTag](../structureddocumenttag/) et [StructuredDocumentTagRangeStart](../structureddocumenttagrangestart/).

```cpp
class IStructuredDocumentTag : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| virtual [get_Appearance](./get_appearance/)() | Obtient ou définit l'apparence de la balise de document structuré. |
| virtual [get_Color](./get_color/)() | Obtient ou définit la couleur de la balise de document structuré. |
| virtual [get_Id](./get_id/)() | Spécifie un identifiant numérique persistant en lecture seule unique pour ce **SDT**. |
| virtual [get_IsMultiSection](./get_ismultisection/)() | Renvoie true si cette instance est une balise de document structuré à portée (multi-section). |
| virtual [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() | Spécifie si le contenu de ce **SDT** doit être interprété comme contenant du texte de substitution (par opposition au texte normal contenu dans le **SDT**). Si la valeur est true, cet état sera réactivé (affichage du texte de substitution) lors de l'ouverture de ce document. |
| virtual [get_Level](./get_level/)() const | Obtient le niveau auquel ce **SDT** apparaît dans l'arborescence du document. |
| virtual [get_LockContentControl](./get_lockcontentcontrol/)() | Lorsque la valeur est true, cette propriété empêchera un utilisateur de supprimer ce **SDT**. |
| virtual [get_LockContents](./get_lockcontents/)() | Lorsque la valeur est true, cette propriété empêchera un utilisateur de modifier le contenu de ce **SDT**. |
| virtual [get_Node](./get_node/)() | Renvoie l'objet [Node](../../aspose.words/node/) qui implémente cette interface. |
| virtual [get_Placeholder](./get_placeholder/)() | Obtient le [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) contenant le texte de substitution qui doit être affiché lorsque le contenu de ce SDT est vide, que l'élément XML mappé associé est vide comme spécifié via l'élément [XmlMapping](./get_xmlmapping/) ou que l'élément [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) est true. |
| virtual [get_PlaceholderName](./get_placeholdername/)() | Obtient ou définit le nom du [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) contenant le texte de substitution. |
| virtual [get_SdtType](./get_sdttype/)() | Obtient le type de cette **Structured document tag**. |
| virtual [get_Tag](./get_tag/)() const | Spécifie une balise associée au nœud SDT actuel. Ne peut pas être null. |
| virtual [get_Title](./get_title/)() const | Spécifie le nom convivial associé à ce **SDT**. Ne peut pas être null. |
| virtual [get_WordOpenXML](./get_wordopenxml/)() | Obtient une chaîne qui représente le XML contenu dans le nœud au format [FlatOpc](../../aspose.words/saveformat/). |
| virtual [get_XmlMapping](./get_xmlmapping/)() | Obtient un objet qui représente le mappage de cette balise de document structuré aux données XML dans une partie XML personnalisée du document actuel. |
| virtual [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) | Renvoie une collection en direct des nœuds enfants correspondant aux types spécifiés. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [RemoveSelfOnly](./removeselfonly/)() | Supprime uniquement ce nœud SDT lui‑-même, mais conserve son contenu dans l'arborescence du document. |
| virtual [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) | Mutateur pour [Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance](./get_appearance/). |
| virtual [set_Color](./set_color/)(System::Drawing::Color) | Mutateur pour [Aspose::Words::Markup::IStructuredDocumentTag::get_Color](./get_color/). |
| virtual [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) | Mutateur pour [Aspose::Words::Markup::IStructuredDocumentTag::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/). |
| virtual [set_LockContentControl](./set_lockcontentcontrol/)(bool) | Mutateur pour [Aspose::Words::Markup::IStructuredDocumentTag::get_LockContentControl](./get_lockcontentcontrol/). |
| virtual [set_LockContents](./set_lockcontents/)(bool) | Mutateur pour [Aspose::Words::Markup::IStructuredDocumentTag::get_LockContents](./get_lockcontents/). |
| virtual [set_PlaceholderName](./set_placeholdername/)(System::String) | Mutateur pour [Aspose::Words::Markup::IStructuredDocumentTag::get_PlaceholderName](./get_placeholdername/). |
| virtual [set_Tag](./set_tag/)(System::String) | Mutateur pour [Aspose::Words::Markup::IStructuredDocumentTag::get_Tag](./get_tag/). |
| virtual [set_Title](./set_title/)(System::String) | Définisseur pour [Aspose::Words::Markup::IStructuredDocumentTag::get_Title](./get_title/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment supprimer la balise de document structuré, mais conserve le contenu à l'intérieur.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// Cette collection fournit une interface unifiée pour accéder aux balises structurées à portée et non à portée.
System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>> sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(5, sdts->LINQ_Count());

// Ici, nous pouvons obtenir les nœuds enfants à partir de l'interface commune des balises structurées à portée et non à portée.
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

## Voir aussi

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
