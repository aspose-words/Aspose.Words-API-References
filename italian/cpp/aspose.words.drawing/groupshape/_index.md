---
title: "Aspose::Words::Drawing::GroupShape class"
linktitle: "GroupShape"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::GroupShape class. Rappresenta un gruppo di forme in un documento. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.drawing/groupshape/
---
## GroupShape class


Rappresenta un gruppo di forme in un documento. Per saperne di più, visita l'articolo di documentazione [How to Add Group Shape into a Word Document](https://docs.aspose.com/words/cpp/how-to-add-group-shape-into-a-word-document/).

```cpp
class GroupShape : public Aspose::Words::Drawing::ShapeBase
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore per visitare la fine del [GroupShape](./). |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore per visitare l'inizio del [GroupShape](./). |
| [AdjustWithEffects](../shapebase/adjustwitheffects/)(System::Drawing::RectangleF) | Aggiunge al rettangolo di origine i valori dell'estensione dell'effetto e restituisce il rettangolo finale. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicato del nodo. |
| [get_AllowOverlap](../shapebase/get_allowoverlap/)() | Ottiene o imposta un valore che specifica se questa forma può sovrapporsi ad altre forme. |
| [get_AlternativeText](../shapebase/get_alternativetext/)() | Definisce il testo alternativo da visualizzare al posto di un'immagine. |
| [get_AnchorLocked](../shapebase/get_anchorlocked/)() | Specifica se l'ancora della forma è bloccata. |
| [get_AspectRatioLocked](../shapebase/get_aspectratiolocked/)() | Specifica se il rapporto d'aspetto della forma è bloccato. |
| [get_BehindText](../shapebase/get_behindtext/)() | Specifica se la forma è sotto o sopra il testo. |
| [get_Bottom](../shapebase/get_bottom/)() | Ottiene la posizione del bordo inferiore del blocco contenitore della forma. |
| [get_Bounds](../shapebase/get_bounds/)() | Ottiene o imposta la posizione e le dimensioni del blocco contenitore della forma. |
| [get_BoundsInPoints](../shapebase/get_boundsinpoints/)() | Ottiene la posizione e le dimensioni del blocco contenitore della forma in punti, relative all'ancora della forma più in alto. |
| [get_BoundsWithEffects](../shapebase/get_boundswitheffects/)() | Ottiene l'estensione finale che questo oggetto forma ha dopo l'applicazione degli effetti di disegno. Il valore è misurato in punti. |
| [get_CanHaveImage](../shapebase/get_canhaveimage/)() | Restituisce **true** se il tipo di forma consente alla forma di avere un'immagine. |
| [get_CoordOrigin](../shapebase/get_coordorigin/)() | Le coordinate nell'angolo in alto a sinistra del blocco contenitore di questa forma. |
| [get_CoordSize](../shapebase/get_coordsize/)() | La larghezza e l'altezza dello spazio di coordinate all'interno del blocco contenitore di questa forma. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Ottiene il numero di figli immediati di questo nodo. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifica un identificatore personalizzato per il nodo. |
| [get_DistanceBottom](../shapebase/get_distancebottom/)() | Restituisce o imposta la distanza (in punti) tra il testo del documento e il bordo inferiore della forma. |
| [get_DistanceLeft](../shapebase/get_distanceleft/)() | Restituisce o imposta la distanza (in punti) tra il testo del documento e il bordo sinistro della forma. |
| [get_DistanceRight](../shapebase/get_distanceright/)() | Restituisce o imposta la distanza (in punti) tra il testo del documento e il bordo destro della forma. |
| [get_DistanceTop](../shapebase/get_distancetop/)() | Restituisce o imposta la distanza (in punti) tra il testo del documento e il bordo superiore della forma. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Ottiene il documento a cui appartiene questo nodo. |
| [get_Fill](../shapebase/get_fill/)() | Ottiene la formattazione di riempimento per la forma. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Ottiene il primo figlio del nodo. |
| [get_FlipOrientation](../shapebase/get_fliporientation/)() | Cambia l'orientamento di una forma. |
| [get_Font](../shapebase/get_font/)() | Fornisce l'accesso alla formattazione del carattere di questo oggetto. |
| [get_Glow](../shapebase/get_glow/)() | Ottiene la formattazione dell'effetto bagliore per la forma. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Restituisce **true** se questo nodo ha dei nodi figli. |
| [get_Height](../shapebase/get_height/)() | Ottiene o imposta l'altezza del blocco contenitore della forma. |
| [get_HeightRelative](../shapebase/get_heightrelative/)() | Ottiene o imposta il valore che rappresenta la percentuale dell'altezza relativa della forma. |
| [get_Hidden](../shapebase/get_hidden/)() | Ottiene o imposta un valore booleano che indica se la forma è visibile. |
| [get_HorizontalAlignment](../shapebase/get_horizontalalignment/)() | Specifica come la forma è posizionata orizzontalmente. |
| [get_HRef](../shapebase/get_href/)() | Ottiene o imposta l'indirizzo completo del collegamento ipertestuale per una forma. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Restituisce **true** poiché questo nodo può avere nodi figli. |
| [get_IsDecorative](../shapebase/get_isdecorative/)() | Ottiene o imposta il flag che specifica se la forma è decorativa nel documento. |
| [get_IsDeleteRevision](../shapebase/get_isdeleterevision/)() | Restituisce true se questo oggetto è stato eliminato in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsGroup](../shapebase/get_isgroup/)() | Restituisce **true** se questa è una forma di gruppo. |
| [get_IsHorizontalRule](../shapebase/get_ishorizontalrule/)() | Restituisce **true** se questa forma è una regola orizzontale. |
| [get_IsImage](../shapebase/get_isimage/)() | Restituisce **true** se questa forma è una forma immagine. |
| [get_IsInline](../shapebase/get_isinline/)() | Un modo rapido per determinare se questa forma è posizionata in linea con il testo. |
| [get_IsInsertRevision](../shapebase/get_isinsertrevision/)() | Restituisce true se questo oggetto è stato inserito in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsLayoutInCell](../shapebase/get_islayoutincell/)() | Ottiene o imposta un flag che indica se la forma è visualizzata all'interno di una tabella o al di fuori di essa. |
| [get_IsMoveFromRevision](../shapebase/get_ismovefromrevision/)() | Restituisce **true** se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsMoveToRevision](../shapebase/get_ismovetorevision/)() | Restituisce **true** se questo oggetto è stato spostato (inserito) in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsSignatureLine](../shapebase/get_issignatureline/)() | Indica che la forma è una [SignatureLine](../signatureline/). |
| [get_IsTopLevel](../shapebase/get_istoplevel/)() | Restituisce **true** se questa forma non è un figlio di una forma di gruppo. |
| [get_IsWordArt](../shapebase/get_iswordart/)() | Restituisce **true** se questa forma è un oggetto WordArt. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Ottiene l'ultimo figlio del nodo. |
| [get_Left](../shapebase/get_left/)() | Ottiene o imposta la posizione del bordo sinistro del blocco contenitore della forma. |
| [get_LeftRelative](../shapebase/get_leftrelative/)() | Ottiene o imposta il valore che rappresenta la posizione sinistra relativa della forma in percentuale. |
| [get_MarkupLanguage](../shapebase/get_markuplanguage/)() const | Ottiene il MarkupLanguage usato per questo oggetto grafico. |
| [get_Name](../shapebase/get_name/)() | Ottiene o imposta il nome opzionale della forma. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Ottiene il nodo immediatamente successivo a questo nodo. |
| [get_NodeType](./get_nodetype/)() const override | Restituisce [GroupShape](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Ottiene il genitore immediato di questo nodo. |
| [get_ParentParagraph](../shapebase/get_parentparagraph/)() | Restituisce il paragrafo genitore immediato. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Ottiene il nodo immediatamente precedente a questo nodo. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Restituisce un oggetto [Range](../../aspose.words/range/) che rappresenta la porzione di un documento contenuta in questo nodo. |
| [get_Reflection](../shapebase/get_reflection/)() | Ottiene la formattazione di riflessione per la forma. |
| [get_RelativeHorizontalPosition](../shapebase/get_relativehorizontalposition/)() | Specifica rispetto a cosa la forma è posizionata orizzontalmente. |
| [get_RelativeHorizontalSize](../shapebase/get_relativehorizontalsize/)() | Ottiene o imposta il valore della dimensione relativa della forma nella direzione orizzontale. |
| [get_RelativeVerticalPosition](../shapebase/get_relativeverticalposition/)() | Specifica rispetto a cosa la forma è posizionata verticalmente. |
| [get_RelativeVerticalSize](../shapebase/get_relativeverticalsize/)() | Ottiene o imposta il valore della dimensione relativa della forma nella direzione verticale. |
| [get_Right](../shapebase/get_right/)() | Ottiene la posizione del bordo destro del blocco contenitore della forma. |
| [get_Rotation](../shapebase/get_rotation/)() | Definisce l'angolo (in gradi) di rotazione di una forma. Un valore positivo corrisponde all'angolo di rotazione in senso orario. |
| [get_ScreenTip](../shapebase/get_screentip/)() | Definisce il testo visualizzato quando il puntatore del mouse si sposta sopra la forma. |
| [get_ShadowFormat](../shapebase/get_shadowformat/)() | Ottiene la formattazione dell'ombra per la forma. |
| [get_ShapeType](../shapebase/get_shapetype/)() | Ottiene il tipo di forma. |
| [get_SizeInPoints](../shapebase/get_sizeinpoints/)() | Ottiene le dimensioni della forma in punti. |
| [get_SoftEdge](../shapebase/get_softedge/)() | Ottiene la formattazione del bordo morbido per la forma. |
| [get_Target](../shapebase/get_target/)() | Ottiene o imposta il frame di destinazione per il collegamento ipertestuale della forma. |
| [get_Title](../shapebase/get_title/)() | Ottiene o imposta il titolo (didascalia) dell'oggetto forma corrente. |
| [get_Top](../shapebase/get_top/)() | Ottiene o imposta la posizione del bordo superiore del blocco contenitore della forma. |
| [get_TopRelative](../shapebase/get_toprelative/)() | Ottiene o imposta il valore che rappresenta la posizione superiore relativa della forma in percentuale. |
| [get_VerticalAlignment](../shapebase/get_verticalalignment/)() | Specifica come la forma è posizionata verticalmente. |
| [get_Width](../shapebase/get_width/)() | Ottiene o imposta la larghezza del blocco contenitore della forma. |
| [get_WidthRelative](../shapebase/get_widthrelative/)() | Ottiene o imposta il valore che rappresenta la percentuale della larghezza relativa della forma. |
| [get_WrapSide](../shapebase/get_wrapside/)() | Specifica come il testo è avvolto attorno alla forma. |
| [get_WrapType](../shapebase/get_wraptype/)() | Definisce se la forma è in linea o flottante. Per le forme flottanti definisce la modalità di avvolgimento del testo attorno alla forma. |
| [get_ZOrder](../shapebase/get_zorder/)() | Determina l'ordine di visualizzazione delle forme sovrapposte. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Ottiene il primo antenato del [NodeType](../../aspose.words/nodetype/) specificato. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Restituisce il nodo figlio N-esimo che corrisponde al tipo specificato. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Restituisce una collezione dinamica di nodi figlio che corrispondono al tipo specificato. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Fornisce supporto per l'iterazione in stile foreach sui nodi figlio di questo nodo. |
| [GetShapeRenderer](../shapebase/getshaperenderer/)() | Crea e restituisce un oggetto che può essere usato per renderizzare questa forma in un'immagine. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [GetType](./gettype/)() const override |  |
| [GroupShape](./groupshape/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Crea una nuova forma di gruppo. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Restituisce l'indice del nodo figlio specificato nell'array dei nodi figlio. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [LocalToParent](../shapebase/localtoparent/)(System::Drawing::PointF) | Converte un valore dallo spazio di coordinate locale allo spazio di coordinate della forma genitore. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo successivo secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Un metodo di utilità che converte un valore enum di tipo nodo in una stringa leggibile dall'utente. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| [Remove](../../aspose.words/node/remove/)() | Rimuove se stesso dal genitore. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Rimuove tutti i nodi figlio del nodo corrente. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Rimuove tutti i nodi discendenti [SmartTag](../../aspose.words.markup/smarttag/) del nodo corrente. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Seleziona il primo [Node](../../aspose.words/node/) che corrisponde all'espressione XPath. |
| [set_AllowOverlap](../shapebase/set_allowoverlap/)(bool) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_AllowOverlap](../shapebase/get_allowoverlap/). |
| [set_AlternativeText](../shapebase/set_alternativetext/)(const System::String\&) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_AlternativeText](../shapebase/get_alternativetext/). |
| [set_AnchorLocked](../shapebase/set_anchorlocked/)(bool) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_AnchorLocked](../shapebase/get_anchorlocked/). |
| [set_AspectRatioLocked](../shapebase/set_aspectratiolocked/)(bool) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked](../shapebase/get_aspectratiolocked/). |
| [set_BehindText](../shapebase/set_behindtext/)(bool) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_BehindText](../shapebase/get_behindtext/). |
| [set_Bounds](../shapebase/set_bounds/)(System::Drawing::RectangleF) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_Bounds](../shapebase/get_bounds/). |
| [set_CoordOrigin](../shapebase/set_coordorigin/)(System::Drawing::Point) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_CoordOrigin](../shapebase/get_coordorigin/). |
| [set_CoordSize](../shapebase/set_coordsize/)(System::Drawing::Size) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_CoordSize](../shapebase/get_coordsize/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter per [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DistanceBottom](../shapebase/set_distancebottom/)(double) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_DistanceBottom](../shapebase/get_distancebottom/). |
| [set_DistanceLeft](../shapebase/set_distanceleft/)(double) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_DistanceLeft](../shapebase/get_distanceleft/). |
| [set_DistanceRight](../shapebase/set_distanceright/)(double) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_DistanceRight](../shapebase/get_distanceright/). |
| [set_DistanceTop](../shapebase/set_distancetop/)(double) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_DistanceTop](../shapebase/get_distancetop/). |
| [set_FlipOrientation](../shapebase/set_fliporientation/)(Aspose::Words::Drawing::FlipOrientation) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_FlipOrientation](../shapebase/get_fliporientation/). |
| [set_Height](../shapebase/set_height/)(double) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_Height](../shapebase/get_height/). |
| [set_HeightRelative](../shapebase/set_heightrelative/)(float) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_HeightRelative](../shapebase/get_heightrelative/). |
| [set_Hidden](../shapebase/set_hidden/)(bool) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_Hidden](../shapebase/get_hidden/). |
| [set_HorizontalAlignment](../shapebase/set_horizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment](../shapebase/get_horizontalalignment/). |
| [set_HRef](../shapebase/set_href/)(const System::String\&) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_HRef](../shapebase/get_href/). |
| [set_IsDecorative](../shapebase/set_isdecorative/)(bool) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_IsDecorative](../shapebase/get_isdecorative/). |
| [set_IsLayoutInCell](../shapebase/set_islayoutincell/)(bool) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell](../shapebase/get_islayoutincell/). |
| [set_Left](../shapebase/set_left/)(double) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_Left](../shapebase/get_left/). |
| [set_LeftRelative](../shapebase/set_leftrelative/)(float) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_LeftRelative](../shapebase/get_leftrelative/). |
| [set_Name](../shapebase/set_name/)(const System::String\&) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_Name](../shapebase/get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalPosition](../shapebase/set_relativehorizontalposition/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition](../shapebase/get_relativehorizontalposition/). |
| [set_RelativeHorizontalSize](../shapebase/set_relativehorizontalsize/)(Aspose::Words::Drawing::RelativeHorizontalSize) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize](../shapebase/get_relativehorizontalsize/). |
| [set_RelativeVerticalPosition](../shapebase/set_relativeverticalposition/)(Aspose::Words::Drawing::RelativeVerticalPosition) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition](../shapebase/get_relativeverticalposition/). |
| [set_RelativeVerticalSize](../shapebase/set_relativeverticalsize/)(Aspose::Words::Drawing::RelativeVerticalSize) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize](../shapebase/get_relativeverticalsize/). |
| [set_Rotation](../shapebase/set_rotation/)(double) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_Rotation](../shapebase/get_rotation/). |
| [set_ScreenTip](../shapebase/set_screentip/)(const System::String\&) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_ScreenTip](../shapebase/get_screentip/). |
| [set_Target](../shapebase/set_target/)(const System::String\&) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_Target](../shapebase/get_target/). |
| [set_Title](../shapebase/set_title/)(const System::String\&) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_Title](../shapebase/get_title/). |
| [set_Top](../shapebase/set_top/)(double) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_Top](../shapebase/get_top/). |
| [set_TopRelative](../shapebase/set_toprelative/)(float) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_TopRelative](../shapebase/get_toprelative/). |
| [set_VerticalAlignment](../shapebase/set_verticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment](../shapebase/get_verticalalignment/). |
| [set_Width](../shapebase/set_width/)(double) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_Width](../shapebase/get_width/). |
| [set_WidthRelative](../shapebase/set_widthrelative/)(float) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_WidthRelative](../shapebase/get_widthrelative/). |
| [set_WrapSide](../shapebase/set_wrapside/)(Aspose::Words::Drawing::WrapSide) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_WrapSide](../shapebase/get_wrapside/). |
| [set_WrapType](../shapebase/set_wraptype/)(Aspose::Words::Drawing::WrapType) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_WrapType](../shapebase/get_wraptype/). |
| [set_ZOrder](../shapebase/set_zorder/)(int32_t) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_ZOrder](../shapebase/get_zorder/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Esporta il contenuto del nodo in una stringa usando le opzioni di salvataggio specificate. |
| static [Type](./type/)() |  |
## Note


Un [GroupShape](./) è un nodo composito e può avere nodi [Shape](../shape/) e [GroupShape](./) come figli.

Ogni [GroupShape](./) definisce un nuovo sistema di coordinate per le sue forme figlie. Il sistema di coordinate è definito usando le proprietà [CoordSize](../shapebase/get_coordsize/) e [CoordOrigin](../shapebase/get_coordorigin/).

## Vedi anche

* Class [ShapeBase](../shapebase/)
* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
