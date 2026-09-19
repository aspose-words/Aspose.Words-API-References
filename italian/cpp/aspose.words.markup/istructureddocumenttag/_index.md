---
title: "Interfaccia Aspose::Words::Markup::IStructuredDocumentTag"
linktitle: "IStructuredDocumentTag"
second_title: "Riferimento API Aspose.Words per C++"
description: "Interfaccia Aspose::Words::Markup::IStructuredDocumentTag. Interfaccia per definire dati comuni per StructuredDocumentTag e StructuredDocumentTagRangeStart in C++."
type: docs
weight: 16000
url: /it/cpp/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface


Interfaccia per definire dati comuni per [StructuredDocumentTag](../structureddocumenttag/) e [StructuredDocumentTagRangeStart](../structureddocumenttagrangestart/).

```cpp
class IStructuredDocumentTag : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| virtual [get_Appearance](./get_appearance/)() | Ottiene o imposta l'aspetto del tag di documento strutturato. |
| virtual [get_Color](./get_color/)() | Ottiene o imposta il colore del tag di documento strutturato. |
| virtual [get_Id](./get_id/)() | Specifica un Id numerico persistente univoco di sola lettura per questo **SDT**. |
| virtual [get_IsMultiSection](./get_ismultisection/)() | Restituisce true se questa istanza è un tag di documento strutturato a intervallo (multi-sezione). |
| virtual [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() | Specifica se il contenuto di questo **SDT** deve essere interpretato come testo segnaposto (invece del normale contenuto testuale all'interno del SDT). Se impostato su true, questo stato verrà ripristinato (mostrando il testo segnaposto) all'apertura di questo documento. |
| virtual [get_Level](./get_level/)() const | Ottiene il livello al quale questo **SDT** si trova nell'albero del documento. |
| virtual [get_LockContentControl](./get_lockcontentcontrol/)() | Quando impostata su true, questa proprietà impedirà a un utente di eliminare questo **SDT**. |
| virtual [get_LockContents](./get_lockcontents/)() | Quando impostata su true, questa proprietà impedirà a un utente di modificare il contenuto di questo **SDT**. |
| virtual [get_Node](./get_node/)() | Restituisce l'oggetto [Node](../../aspose.words/node/) che implementa questa interfaccia. |
| virtual [get_Placeholder](./get_placeholder/)() | Ottiene il [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) contenente il testo segnaposto che dovrebbe essere visualizzato quando il contenuto di questo SDT è vuoto, l'elemento XML mappato associato è vuoto come specificato tramite l'elemento [XmlMapping](./get_xmlmapping/) o l'elemento [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) è true. |
| virtual [get_PlaceholderName](./get_placeholdername/)() | Ottiene o imposta il Nome del [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) contenente il testo segnaposto. |
| virtual [get_SdtType](./get_sdttype/)() | Ottiene il tipo di questo **Structured document tag**. |
| virtual [get_Tag](./get_tag/)() const | Specifica un tag associato al nodo SDT corrente. Non può essere null. |
| virtual [get_Title](./get_title/)() const | Specifica il nome descrittivo associato a questo **SDT**. Non può essere null. |
| virtual [get_WordOpenXML](./get_wordopenxml/)() | Ottiene una stringa che rappresenta l'XML contenuto nel nodo nel formato [FlatOpc](../../aspose.words/saveformat/). |
| virtual [get_XmlMapping](./get_xmlmapping/)() | Ottiene un oggetto che rappresenta la mappatura di questo tag di documento strutturato ai dati XML in una parte XML personalizzata del documento corrente. |
| virtual [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) | Restituisce una collezione live di nodi figlio che corrispondono ai tipi specificati. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [RemoveSelfOnly](./removeselfonly/)() | Rimuove solo questo nodo SDT, ma mantiene il suo contenuto all'interno dell'albero del documento. |
| virtual [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) | Setter per [Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance](./get_appearance/). |
| virtual [set_Color](./set_color/)(System::Drawing::Color) | Setter per [Aspose::Words::Markup::IStructuredDocumentTag::get_Color](./get_color/). |
| virtual [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) | Setter per [Aspose::Words::Markup::IStructuredDocumentTag::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/). |
| virtual [set_LockContentControl](./set_lockcontentcontrol/)(bool) | Setter per [Aspose::Words::Markup::IStructuredDocumentTag::get_LockContentControl](./get_lockcontentcontrol/). |
| virtual [set_LockContents](./set_lockcontents/)(bool) | Setter per [Aspose::Words::Markup::IStructuredDocumentTag::get_LockContents](./get_lockcontents/). |
| virtual [set_PlaceholderName](./set_placeholdername/)(System::String) | Setter per [Aspose::Words::Markup::IStructuredDocumentTag::get_PlaceholderName](./get_placeholdername/). |
| virtual [set_Tag](./set_tag/)(System::String) | Setter per [Aspose::Words::Markup::IStructuredDocumentTag::get_Tag](./get_tag/). |
| virtual [set_Title](./set_title/)(System::String) | Impostatore per [Aspose::Words::Markup::IStructuredDocumentTag::get_Title](./get_title/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come rimuovere il tag di documento strutturato, ma mantiene il contenuto interno.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// Questa collezione fornisce un'interfaccia unificata per accedere ai tag strutturati con intervallo e senza intervallo.
System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>> sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(5, sdts->LINQ_Count());

// Qui possiamo ottenere i nodi figlio dall'interfaccia comune dei tag strutturati con intervallo e senza intervallo.
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

## Vedi anche

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
