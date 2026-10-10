---
title: "Classe Aspose::Words::Markup::StructuredDocumentTag"
linktitle: "StructuredDocumentTag"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Markup::StructuredDocumentTag. Rappresenta un tag di documento strutturato (SDT o controllo di contenuto) in un documento. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class


Rappresenta un tag di documento strutturato (SDT o controllo del contenuto) in un documento. Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class StructuredDocumentTag : public Aspose::Words::CompositeNode,
                              public Aspose::Words::Markup::IMarkupNode,
                              public Aspose::Words::Revisions::ITrackableNode,
                              public Aspose::Words::IRunAttrSource,
                              public Aspose::Words::Markup::IStructuredDocumentTag
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore per visitare la fine del [StructuredDocumentTag](./). |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore per visitare l'inizio del [StructuredDocumentTag](./). |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clear](./clear/)() | Cancella il contenuto di questo tag di documento strutturato e visualizza un segnaposto se è definito. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicato del nodo. |
| [get_Appearance](./get_appearance/)() override | Ottiene/Imposta l'aspetto di un tag di documento strutturato. |
| [get_BuildingBlockCategory](./get_buildingblockcategory/)() | Specifica la categoria del blocco di costruzione per questo nodo **SDT**. Non può essere **null**. |
| [get_BuildingBlockGallery](./get_buildingblockgallery/)() | Specifica il tipo di blocco di costruzione per questo **SDT**. Non può essere **null**. |
| [get_CalendarType](./get_calendartype/)() | Specifica il tipo di calendario per questo **SDT**. Il valore predefinito è [Default](../sdtcalendartype/) |
| [get_Checked](./get_checked/)() | Ottiene/Imposta lo stato corrente della casella di controllo **SDT**. Il valore predefinito per questa proprietà è **false**. |
| [get_Color](./get_color/)() override | Ottiene o imposta il colore del tag di documento strutturato. |
| [get_ContentsFont](./get_contentsfont/)() | [Font](../../aspose.words/font/) formattazione che verrà applicata al testo inserito in **SDT**. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Ottiene il numero di figli immediati di questo nodo. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifica un identificatore personalizzato per il nodo. |
| [get_DateDisplayFormat](./get_datedisplayformat/)() | Stringa che rappresenta il formato in cui le date sono visualizzate. |
| [get_DateDisplayLocale](./get_datedisplaylocale/)() | Consente di impostare/ottenere il formato linguistico per la data visualizzata in questo **SDT**. |
| [get_DateStorageFormat](./get_datestorageformat/)() | Ottiene/Imposta il formato in cui la data per un SDT data è memorizzata quando il **SDT** è collegato a un nodo XML nell'archivio dati del documento. Il valore predefinito è [DateTime](../sdtdatestorageformat/) |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Ottiene il documento a cui appartiene questo nodo. |
| [get_EndCharacterFont](./get_endcharacterfont/)() | [Font](../../aspose.words/font/) formattazione che verrà applicata all'ultimo carattere del testo inserito in **SDT**. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Ottiene il primo figlio del nodo. |
| [get_FullDate](./get_fulldate/)() | Specifica la data e l'ora complete inserite più recentemente in questo **SDT**. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Restituisce **true** se questo nodo ha dei nodi figli. |
| [get_Id](./get_id/)() override | Specifica un Id numerico persistente univoco di sola lettura per questo **SDT**. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Restituisce **true** poiché questo nodo può avere nodi figli. |
| [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() override | Specifica se il contenuto di questo **SDT** deve essere interpretato come testo segnaposto (invece del normale contenuto testuale all'interno del SDT). Se impostato su **true**, questo stato verrà ripristinato (mostrando il testo segnaposto) all'apertura di questo documento. |
| [get_IsTemporary](./get_istemporary/)() const | Specifica se questo **SDT** deve essere rimosso dal documento WordProcessingML quando il suo contenuto viene modificato. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Ottiene l'ultimo figlio del nodo. |
| [get_Level](./get_level/)() const override | Ottiene il livello al quale questo **SDT** si trova nell'albero del documento. |
| [get_ListItems](./get_listitems/)() | Ottiene [SdtListItemCollection](../sdtlistitemcollection/) associato a questo **SDT**. |
| [get_LockContentControl](./get_lockcontentcontrol/)() override | Quando impostato su **true**, questa proprietà impedirà a un utente di eliminare questo **SDT**. |
| [get_LockContents](./get_lockcontents/)() override | Quando impostato su **true**, questa proprietà impedirà a un utente di modificare il contenuto di questo **SDT**. |
| [get_Multiline](./get_multiline/)() | Specifica se questo **SDT** consente più righe di testo. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Ottiene il nodo immediatamente successivo a questo nodo. |
| [get_NodeType](./get_nodetype/)() const override | Restituisce [StructuredDocumentTag](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Ottiene il genitore immediato di questo nodo. |
| [get_Placeholder](./get_placeholder/)() override | Ottiene il [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) contenente il testo segnaposto che dovrebbe essere visualizzato quando il contenuto di questo SDT è vuoto, l'elemento XML mappato associato è vuoto come specificato tramite l'elemento [XmlMapping](./get_xmlmapping/) o l'elemento [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) è **true**. |
| [get_PlaceholderName](./get_placeholdername/)() override | Ottiene o imposta il Nome del [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) contenente il testo segnaposto. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Ottiene il nodo immediatamente precedente a questo nodo. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Restituisce un oggetto [Range](../../aspose.words/range/) che rappresenta la porzione di un documento contenuta in questo nodo. |
| [get_SdtType](./get_sdttype/)() override | Ottiene il tipo di questo **Structured document tag**. |
| [get_Style](./get_style/)() | Ottiene o imposta lo [Style](../../aspose.words/style/) del tag di documento strutturato. |
| [get_StyleName](./get_stylename/)() | Ottiene o imposta il nome dello stile applicato al tag di documento strutturato. |
| [get_Tag](./get_tag/)() const override | Specifica un tag associato al nodo SDT corrente. Non può essere **null**. |
| [get_Title](./get_title/)() const override | Specifica il nome descrittivo associato a questo **SDT**. Non può essere **null**. |
| [get_WordOpenXML](./get_wordopenxml/)() override | Ottiene una stringa che rappresenta l'XML contenuto nel nodo nel formato [FlatOpc](../../aspose.words/saveformat/). |
| [get_WordOpenXMLMinimal](./get_wordopenxmlminimal/)() | Ottiene una stringa che rappresenta l'XML contenuto nel nodo nel formato [FlatOpc](../../aspose.words/saveformat/). A differenza della proprietà [WordOpenXML](./get_wordopenxml/), questo metodo genera un documento semplificato che esclude tutte le parti non relative al contenuto. |
| [get_XmlMapping](./get_xmlmapping/)() override | Ottiene un oggetto che rappresenta la mappatura di questo tag di documento strutturato ai dati XML in una parte XML personalizzata del documento corrente. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Ottiene il primo antenato del [NodeType](../../aspose.words/nodetype/) specificato. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Restituisce il nodo figlio N-esimo che corrisponde al tipo specificato. |
| [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) override | Restituisce una collezione dinamica di nodi figlio che corrispondono al tipo specificato. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Fornisce supporto per l'iterazione in stile foreach sui nodi figlio di questo nodo. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Restituisce l'indice del nodo figlio specificato nell'array dei nodi figlio. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo successivo secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Un metodo di utilità che converte un valore enum di tipo nodo in una stringa leggibile dall'utente. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| [Remove](../../aspose.words/node/remove/)() | Rimuove se stesso dal genitore. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Rimuove tutti i nodi figlio del nodo corrente. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSelfOnly](./removeselfonly/)() override | Rimuove solo questo nodo SDT, ma mantiene il suo contenuto all'interno dell'albero del documento. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Rimuove tutti i nodi discendenti [SmartTag](../smarttag/) del nodo corrente. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Seleziona il primo [Node](../../aspose.words/node/) che corrisponde all'espressione XPath. |
| [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) override | Setter per [Aspose::Words::Markup::StructuredDocumentTag::get_Appearance](./get_appearance/). |
| [set_BuildingBlockCategory](./set_buildingblockcategory/)(const System::String\&) | Setter per [Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory](./get_buildingblockcategory/). |
| [set_BuildingBlockGallery](./set_buildingblockgallery/)(const System::String\&) | Setter per [Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery](./get_buildingblockgallery/). |
| [set_CalendarType](./set_calendartype/)(Aspose::Words::Markup::SdtCalendarType) | Setter per [Aspose::Words::Markup::StructuredDocumentTag::get_CalendarType](./get_calendartype/). |
| [set_Checked](./set_checked/)(bool) | Setter per [Aspose::Words::Markup::StructuredDocumentTag::get_Checked](./get_checked/). |
| [set_Color](./set_color/)(System::Drawing::Color) override | Setter per [Aspose::Words::Markup::StructuredDocumentTag::get_Color](./get_color/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter per [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DateDisplayFormat](./set_datedisplayformat/)(const System::String\&) | Setter per [Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayFormat](./get_datedisplayformat/). |
| [set_DateDisplayLocale](./set_datedisplaylocale/)(int32_t) | Setter per [Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayLocale](./get_datedisplaylocale/). |
| [set_DateStorageFormat](./set_datestorageformat/)(Aspose::Words::Markup::SdtDateStorageFormat) | Setter per [Aspose::Words::Markup::StructuredDocumentTag::get_DateStorageFormat](./get_datestorageformat/). |
| [set_FullDate](./set_fulldate/)(System::DateTime) | Setter per [Aspose::Words::Markup::StructuredDocumentTag::get_FullDate](./get_fulldate/). |
| [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) override | Setter per [Aspose::Words::Markup::StructuredDocumentTag::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/). |
| [set_IsTemporary](./set_istemporary/)(bool) | Setter per [Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary](./get_istemporary/). |
| [set_LockContentControl](./set_lockcontentcontrol/)(bool) override | Setter per [Aspose::Words::Markup::StructuredDocumentTag::get_LockContentControl](./get_lockcontentcontrol/). |
| [set_LockContents](./set_lockcontents/)(bool) override | Setter per [Aspose::Words::Markup::StructuredDocumentTag::get_LockContents](./get_lockcontents/). |
| [set_Multiline](./set_multiline/)(bool) | Setter per [Aspose::Words::Markup::StructuredDocumentTag::get_Multiline](./get_multiline/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PlaceholderName](./set_placeholdername/)(System::String) override | Setter per [Aspose::Words::Markup::StructuredDocumentTag::get_PlaceholderName](./get_placeholdername/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Impostatore per [Aspose::Words::Markup::StructuredDocumentTag::get_Style](./get_style/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Impostatore per [Aspose::Words::Markup::StructuredDocumentTag::get_StyleName](./get_stylename/). |
| [set_Tag](./set_tag/)(System::String) override | Impostatore per [Aspose::Words::Markup::StructuredDocumentTag::get_Tag](./get_tag/). |
| [set_Title](./set_title/)(System::String) override | Impostatore per [Aspose::Words::Markup::StructuredDocumentTag::get_Title](./get_title/). |
| [SetCheckedSymbol](./setcheckedsymbol/)(int32_t, const System::String\&) | Imposta il simbolo usato per rappresentare lo stato selezionato di un controllo casella di controllo. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SetUncheckedSymbol](./setuncheckedsymbol/)(int32_t, const System::String\&) | Imposta il simbolo usato per rappresentare lo stato non selezionato di un controllo casella di controllo. |
| [StructuredDocumentTag](./structureddocumenttag/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Markup::SdtType, Aspose::Words::Markup::MarkupLevel) | Inizializza una nuova istanza della classe **Structured document tag**. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Esporta il contenuto del nodo in una stringa usando le opzioni di salvataggio specificate. |
| static [Type](./type/)() |  |
## Note


I tag di documento strutturato (SDT) consentono di incorporare semantica definita dal cliente così come il loro comportamento e aspetto in un documento.

In questa versione Aspose.Words fornisce numerosi metodi e proprietà pubblici per manipolare il comportamento e il contenuto di [StructuredDocumentTag](./). La mappatura dei nodi SDT a pacchetti XML personalizzati all'interno di un documento può essere eseguita utilizzando la proprietà [XmlMapping](./get_xmlmapping/).

[StructuredDocumentTag](./) can occur in a document in the following places:

* Block-level - Among paragraphs and tables, as a child of a [Body](../../aspose.words/body/), [HeaderFooter](../../aspose.words/headerfooter/), [Comment](../../aspose.words/comment/), [Footnote](../../aspose.words.notes/footnote/) or a [Shape](../../aspose.words.drawing/shape/) node.
* Row-level - Among rows in a table, as a child of a [Table](../../aspose.words.tables/table/) node.
* Cell-level - Among cells in a table row, as a child of a [Row](../../aspose.words.tables/row/) node.
* Inline-level - Among inline content inside, as a child of a [Paragraph](../../aspose.words/paragraph/).
* Nested inside another [StructuredDocumentTag](./).



## Esempi



Mostra come lavorare con gli stili per gli elementi di controllo del contenuto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Di seguito sono riportati due modi per applicare uno stile dal documento a un tag di documento strutturato.
// 1 -  Applica un oggetto stile dalla collezione di stili del documento:
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Riferisci uno stile nel documento per nome:
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

## Vedi anche

* Class [CompositeNode](../../aspose.words/compositenode/)
* Interface [IStructuredDocumentTag](../istructureddocumenttag/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
