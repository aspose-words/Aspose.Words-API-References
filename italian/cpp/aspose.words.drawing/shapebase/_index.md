---
title: "Aspose::Words::Drawing::ShapeBase class"
linktitle: "ShapeBase"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShapeBase class. Classe base per gli oggetti nello strato di disegno, come un AutoShape, forma libera, oggetto OLE, controllo ActiveX o immagine. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.drawing/shapebase/
---
## ShapeBase class


Classe base per gli oggetti nel livello di disegno, come un'AutoShape, una forma libera, un oggetto OLE, un controllo ActiveX o un'immagine. Per saperne di più, visita l'articolo di documentazione [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class ShapeBase : public Aspose::Words::CompositeNode,
                  public Aspose::Words::IInline,
                  public Aspose::Words::Drawing::Core::IShape,
                  public Aspose::Words::IShapeAttrSource,
                  public Aspose::Words::Revisions::ITrackableNode,
                  public Aspose::Words::Drawing::Core::IFillable,
                  public Aspose::Words::Drawing::Core::IGlow,
                  public Aspose::Words::Drawing::Core::IReflection,
                  public Aspose::Words::Drawing::Core::ISoftEdge,
                  public Aspose::Words::Drawing::Core::IShadow
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| virtual [Accept](../../aspose.words/node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accetta un visitatore. |
| virtual [AcceptEnd](../../aspose.words/compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Quando implementato in una classe derivata, chiama il metodo VisitXXXEnd del visitatore di documento specificato. |
| virtual [AcceptStart](../../aspose.words/compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Quando implementato in una classe derivata, chiama il metodo VisitXXXStart del visitatore di documento specificato. |
| [AdjustWithEffects](./adjustwitheffects/)(System::Drawing::RectangleF) | Aggiunge al rettangolo di origine i valori dell'estensione dell'effetto e restituisce il rettangolo finale. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicato del nodo. |
| [get_AllowOverlap](./get_allowoverlap/)() | Ottiene o imposta un valore che specifica se questa forma può sovrapporsi ad altre forme. |
| [get_AlternativeText](./get_alternativetext/)() | Definisce il testo alternativo da visualizzare al posto di un'immagine. |
| [get_AnchorLocked](./get_anchorlocked/)() | Specifica se l'ancora della forma è bloccata. |
| [get_AspectRatioLocked](./get_aspectratiolocked/)() | Specifica se il rapporto d'aspetto della forma è bloccato. |
| [get_BehindText](./get_behindtext/)() | Specifica se la forma è sotto o sopra il testo. |
| [get_Bottom](./get_bottom/)() | Ottiene la posizione del bordo inferiore del blocco contenitore della forma. |
| [get_Bounds](./get_bounds/)() | Ottiene o imposta la posizione e le dimensioni del blocco contenitore della forma. |
| [get_BoundsInPoints](./get_boundsinpoints/)() | Ottiene la posizione e le dimensioni del blocco contenitore della forma in punti, relative all'ancora della forma più in alto. |
| [get_BoundsWithEffects](./get_boundswitheffects/)() | Ottiene l'estensione finale che questo oggetto forma ha dopo l'applicazione degli effetti di disegno. Il valore è misurato in punti. |
| [get_CanHaveImage](./get_canhaveimage/)() | Restituisce **true** se il tipo di forma consente alla forma di avere un'immagine. |
| [get_CoordOrigin](./get_coordorigin/)() | Le coordinate nell'angolo in alto a sinistra del blocco contenitore di questa forma. |
| [get_CoordSize](./get_coordsize/)() | La larghezza e l'altezza dello spazio di coordinate all'interno del blocco contenitore di questa forma. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Ottiene il numero di figli immediati di questo nodo. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifica un identificatore personalizzato per il nodo. |
| [get_DistanceBottom](./get_distancebottom/)() | Restituisce o imposta la distanza (in punti) tra il testo del documento e il bordo inferiore della forma. |
| [get_DistanceLeft](./get_distanceleft/)() | Restituisce o imposta la distanza (in punti) tra il testo del documento e il bordo sinistro della forma. |
| [get_DistanceRight](./get_distanceright/)() | Restituisce o imposta la distanza (in punti) tra il testo del documento e il bordo destro della forma. |
| [get_DistanceTop](./get_distancetop/)() | Restituisce o imposta la distanza (in punti) tra il testo del documento e il bordo superiore della forma. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Ottiene il documento a cui appartiene questo nodo. |
| [get_Fill](./get_fill/)() | Ottiene la formattazione di riempimento per la forma. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Ottiene il primo figlio del nodo. |
| [get_FlipOrientation](./get_fliporientation/)() | Cambia l'orientamento di una forma. |
| [get_Font](./get_font/)() | Fornisce l'accesso alla formattazione del carattere di questo oggetto. |
| [get_Glow](./get_glow/)() | Ottiene la formattazione dell'effetto bagliore per la forma. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Restituisce **true** se questo nodo ha dei nodi figli. |
| [get_Height](./get_height/)() | Ottiene o imposta l'altezza del blocco contenitore della forma. |
| [get_HeightRelative](./get_heightrelative/)() | Ottiene o imposta il valore che rappresenta la percentuale dell'altezza relativa della forma. |
| [get_Hidden](./get_hidden/)() | Ottiene o imposta un valore booleano che indica se la forma è visibile. |
| [get_HorizontalAlignment](./get_horizontalalignment/)() | Specifica come la forma è posizionata orizzontalmente. |
| [get_HRef](./get_href/)() | Ottiene o imposta l'indirizzo completo del collegamento ipertestuale per una forma. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Restituisce **true** poiché questo nodo può avere nodi figli. |
| [get_IsDecorative](./get_isdecorative/)() | Ottiene o imposta il flag che specifica se la forma è decorativa nel documento. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Restituisce true se questo oggetto è stato eliminato in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsGroup](./get_isgroup/)() | Restituisce **true** se questa è una forma di gruppo. |
| [get_IsHorizontalRule](./get_ishorizontalrule/)() | Restituisce **true** se questa forma è una regola orizzontale. |
| [get_IsImage](./get_isimage/)() | Restituisce **true** se questa forma è una forma immagine. |
| [get_IsInline](./get_isinline/)() | Un modo rapido per determinare se questa forma è posizionata in linea con il testo. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Restituisce true se questo oggetto è stato inserito in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsLayoutInCell](./get_islayoutincell/)() | Ottiene o imposta un flag che indica se la forma è visualizzata all'interno di una tabella o al di fuori di essa. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Restituisce **true** se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Restituisce **true** se questo oggetto è stato spostato (inserito) in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsSignatureLine](./get_issignatureline/)() | Indica che la forma è una [SignatureLine](../signatureline/). |
| [get_IsTopLevel](./get_istoplevel/)() | Restituisce **true** se questa forma non è un figlio di una forma di gruppo. |
| [get_IsWordArt](./get_iswordart/)() | Restituisce **true** se questa forma è un oggetto WordArt. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Ottiene l'ultimo figlio del nodo. |
| [get_Left](./get_left/)() | Ottiene o imposta la posizione del bordo sinistro del blocco contenitore della forma. |
| [get_LeftRelative](./get_leftrelative/)() | Ottiene o imposta il valore che rappresenta la posizione sinistra relativa della forma in percentuale. |
| [get_MarkupLanguage](./get_markuplanguage/)() const | Ottiene il MarkupLanguage usato per questo oggetto grafico. |
| [get_Name](./get_name/)() | Ottiene o imposta il nome opzionale della forma. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Ottiene il nodo immediatamente successivo a questo nodo. |
| virtual [get_NodeType](../../aspose.words/node/get_nodetype/)() const | Ottiene il tipo di questo nodo. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Ottiene il genitore immediato di questo nodo. |
| [get_ParentParagraph](./get_parentparagraph/)() | Restituisce il paragrafo genitore immediato. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Ottiene il nodo immediatamente precedente a questo nodo. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Restituisce un oggetto [Range](../../aspose.words/range/) che rappresenta la porzione di un documento contenuta in questo nodo. |
| [get_Reflection](./get_reflection/)() | Ottiene la formattazione di riflessione per la forma. |
| [get_RelativeHorizontalPosition](./get_relativehorizontalposition/)() | Specifica rispetto a cosa la forma è posizionata orizzontalmente. |
| [get_RelativeHorizontalSize](./get_relativehorizontalsize/)() | Ottiene o imposta il valore della dimensione relativa della forma nella direzione orizzontale. |
| [get_RelativeVerticalPosition](./get_relativeverticalposition/)() | Specifica rispetto a cosa la forma è posizionata verticalmente. |
| [get_RelativeVerticalSize](./get_relativeverticalsize/)() | Ottiene o imposta il valore della dimensione relativa della forma nella direzione verticale. |
| [get_Right](./get_right/)() | Ottiene la posizione del bordo destro del blocco contenitore della forma. |
| [get_Rotation](./get_rotation/)() | Definisce l'angolo (in gradi) di rotazione di una forma. Un valore positivo corrisponde all'angolo di rotazione in senso orario. |
| [get_ScreenTip](./get_screentip/)() | Definisce il testo visualizzato quando il puntatore del mouse si sposta sopra la forma. |
| [get_ShadowFormat](./get_shadowformat/)() | Ottiene la formattazione dell'ombra per la forma. |
| [get_ShapeType](./get_shapetype/)() | Ottiene il tipo di forma. |
| [get_SizeInPoints](./get_sizeinpoints/)() | Ottiene le dimensioni della forma in punti. |
| [get_SoftEdge](./get_softedge/)() | Ottiene la formattazione del bordo morbido per la forma. |
| [get_Target](./get_target/)() | Ottiene o imposta il frame di destinazione per il collegamento ipertestuale della forma. |
| [get_Title](./get_title/)() | Ottiene o imposta il titolo (didascalia) dell'oggetto forma corrente. |
| [get_Top](./get_top/)() | Ottiene o imposta la posizione del bordo superiore del blocco contenitore della forma. |
| [get_TopRelative](./get_toprelative/)() | Ottiene o imposta il valore che rappresenta la posizione superiore relativa della forma in percentuale. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Specifica come la forma è posizionata verticalmente. |
| [get_Width](./get_width/)() | Ottiene o imposta la larghezza del blocco contenitore della forma. |
| [get_WidthRelative](./get_widthrelative/)() | Ottiene o imposta il valore che rappresenta la percentuale della larghezza relativa della forma. |
| [get_WrapSide](./get_wrapside/)() | Specifica come il testo è avvolto attorno alla forma. |
| [get_WrapType](./get_wraptype/)() | Definisce se la forma è in linea o flottante. Per le forme flottanti definisce la modalità di avvolgimento del testo attorno alla forma. |
| [get_ZOrder](./get_zorder/)() | Determina l'ordine di visualizzazione delle forme sovrapposte. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Ottiene il primo antenato del [NodeType](../../aspose.words/nodetype/) specificato. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Restituisce il nodo figlio N-esimo che corrisponde al tipo specificato. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Restituisce una collezione dinamica di nodi figlio che corrispondono al tipo specificato. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Fornisce supporto per l'iterazione in stile foreach sui nodi figlio di questo nodo. |
| [GetShapeRenderer](./getshaperenderer/)() | Crea e restituisce un oggetto che può essere usato per renderizzare questa forma in un'immagine. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Restituisce l'indice del nodo figlio specificato nell'array dei nodi figlio. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [LocalToParent](./localtoparent/)(System::Drawing::PointF) | Converte un valore dallo spazio di coordinate locale allo spazio di coordinate della forma genitore. |
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
| [set_AllowOverlap](./set_allowoverlap/)(bool) | Metodo set per [Aspose::Words::Drawing::ShapeBase::get_AllowOverlap](./get_allowoverlap/). |
| [set_AlternativeText](./set_alternativetext/)(const System::String\&) | Metodo set per [Aspose::Words::Drawing::ShapeBase::get_AlternativeText](./get_alternativetext/). |
| [set_AnchorLocked](./set_anchorlocked/)(bool) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_AnchorLocked](./get_anchorlocked/). |
| [set_AspectRatioLocked](./set_aspectratiolocked/)(bool) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked](./get_aspectratiolocked/). |
| [set_BehindText](./set_behindtext/)(bool) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_BehindText](./get_behindtext/). |
| [set_Bounds](./set_bounds/)(System::Drawing::RectangleF) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_Bounds](./get_bounds/). |
| [set_CoordOrigin](./set_coordorigin/)(System::Drawing::Point) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_CoordOrigin](./get_coordorigin/). |
| [set_CoordSize](./set_coordsize/)(System::Drawing::Size) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_CoordSize](./get_coordsize/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter per [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DistanceBottom](./set_distancebottom/)(double) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_DistanceBottom](./get_distancebottom/). |
| [set_DistanceLeft](./set_distanceleft/)(double) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_DistanceLeft](./get_distanceleft/). |
| [set_DistanceRight](./set_distanceright/)(double) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_DistanceRight](./get_distanceright/). |
| [set_DistanceTop](./set_distancetop/)(double) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_DistanceTop](./get_distancetop/). |
| [set_FlipOrientation](./set_fliporientation/)(Aspose::Words::Drawing::FlipOrientation) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_FlipOrientation](./get_fliporientation/). |
| [set_Height](./set_height/)(double) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_Height](./get_height/). |
| [set_HeightRelative](./set_heightrelative/)(float) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_HeightRelative](./get_heightrelative/). |
| [set_Hidden](./set_hidden/)(bool) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_Hidden](./get_hidden/). |
| [set_HorizontalAlignment](./set_horizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment](./get_horizontalalignment/). |
| [set_HRef](./set_href/)(const System::String\&) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_HRef](./get_href/). |
| [set_IsDecorative](./set_isdecorative/)(bool) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_IsDecorative](./get_isdecorative/). |
| [set_IsLayoutInCell](./set_islayoutincell/)(bool) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell](./get_islayoutincell/). |
| [set_Left](./set_left/)(double) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_Left](./get_left/). |
| [set_LeftRelative](./set_leftrelative/)(float) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_LeftRelative](./get_leftrelative/). |
| [set_Name](./set_name/)(const System::String\&) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_Name](./get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalPosition](./set_relativehorizontalposition/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition](./get_relativehorizontalposition/). |
| [set_RelativeHorizontalSize](./set_relativehorizontalsize/)(Aspose::Words::Drawing::RelativeHorizontalSize) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize](./get_relativehorizontalsize/). |
| [set_RelativeVerticalPosition](./set_relativeverticalposition/)(Aspose::Words::Drawing::RelativeVerticalPosition) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition](./get_relativeverticalposition/). |
| [set_RelativeVerticalSize](./set_relativeverticalsize/)(Aspose::Words::Drawing::RelativeVerticalSize) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize](./get_relativeverticalsize/). |
| [set_Rotation](./set_rotation/)(double) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_Rotation](./get_rotation/). |
| [set_ScreenTip](./set_screentip/)(const System::String\&) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_ScreenTip](./get_screentip/). |
| [set_Target](./set_target/)(const System::String\&) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_Target](./get_target/). |
| [set_Title](./set_title/)(const System::String\&) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_Title](./get_title/). |
| [set_Top](./set_top/)(double) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_Top](./get_top/). |
| [set_TopRelative](./set_toprelative/)(float) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_TopRelative](./get_toprelative/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment](./get_verticalalignment/). |
| [set_Width](./set_width/)(double) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_Width](./get_width/). |
| [set_WidthRelative](./set_widthrelative/)(float) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_WidthRelative](./get_widthrelative/). |
| [set_WrapSide](./set_wrapside/)(Aspose::Words::Drawing::WrapSide) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_WrapSide](./get_wrapside/). |
| [set_WrapType](./set_wraptype/)(Aspose::Words::Drawing::WrapType) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_WrapType](./get_wraptype/). |
| [set_ZOrder](./set_zorder/)(int32_t) | Impostatore per [Aspose::Words::Drawing::ShapeBase::get_ZOrder](./get_zorder/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Esporta il contenuto del nodo in una stringa usando le opzioni di salvataggio specificate. |
| static [Type](./type/)() |  |
## Note


Questa è una classe astratta. Le due classi derivate che è possibile istanziare sono [Shape](../shape/) e [GroupShape](../groupshape/).

Una forma è un nodo nell'albero del documento.

Se la forma è un figlio di un oggetto [Paragraph](../../aspose.words/paragraph/), allora la forma si dice \"top-level\". Le forme di livello superiore sono misurate e posizionate in punti.

Una forma può anche comparire come figlio di un oggetto [GroupShape](../groupshape/) quando più forme sono raggruppate. Le forme figlio di un gruppo sono posizionate nello spazio coordinato e nelle unità definite dalle proprietà [CoordSize](./get_coordsize/) e [CoordOrigin](./get_coordorigin/) del gruppo genitore.

Una forma può essere posizionata in linea con il testo o flottante. Il metodo di posizionamento è controllato tramite la proprietà [WrapType](./get_wraptype/).

Quando una forma è flottante, è posizionata in relazione a qualcosa (ad esempio il paragrafo corrente, il margine o la pagina). Il posizionamento relativo della forma è specificato usando le proprietà [RelativeHorizontalPosition](./get_relativehorizontalposition/) e [RelativeVerticalPosition](./get_relativeverticalposition/).

Una forma flottante può essere posizionata esplicitamente usando le proprietà [Left](./get_left/) e [Top](./get_top/) o allineata in relazione a qualche altro oggetto usando le proprietà [HorizontalAlignment](./get_horizontalalignment/) e [VerticalAlignment](./get_verticalalignment/).

## Esempi



Mostra come inserire un'immagine flottante al centro di una pagina.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un'immagine flottante che apparirà dietro il testo sovrapposto e allineala al centro della pagina.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## Vedi anche

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
