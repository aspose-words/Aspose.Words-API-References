---
title: "Aspose::Words::Drawing::ShapeBase class"
linktitle: "ShapeBase"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase class. Classe de base pour les objets dans le calque de dessin, tels qu'une AutoShape, une forme libre, un objet OLE, un contrôle ActiveX ou une image. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words.drawing/shapebase/
---
## ShapeBase class


Classe de base pour les objets du calque de dessin, tels qu'une AutoShape, une forme libre, un objet OLE, un contrôle ActiveX ou une image. Pour en savoir plus, consultez l'article de documentation [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/) .

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

## Méthodes

| Méthode | Description |
| --- | --- |
| virtual [Accept](../../aspose.words/node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accepte un visiteur. |
| virtual [AcceptEnd](../../aspose.words/compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Lorsqu'il est implémenté dans une classe dérivée, appelle la méthode VisitXXXEnd du visiteur de document spécifié. |
| virtual [AcceptStart](../../aspose.words/compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Lorsqu'il est implémenté dans une classe dérivée, appelle la méthode VisitXXXStart du visiteur de document spécifié. |
| [AdjustWithEffects](./adjustwitheffects/)(System::Drawing::RectangleF) | Ajoute aux valeurs du rectangle source l'étendue de l'effet et renvoie le rectangle final. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un duplicata du nœud. |
| [get_AllowOverlap](./get_allowoverlap/)() | Obtient ou définit une valeur qui indique si cette forme peut chevaucher d'autres formes. |
| [get_AlternativeText](./get_alternativetext/)() | Définit le texte alternatif à afficher à la place d'un graphique. |
| [get_AnchorLocked](./get_anchorlocked/)() | Spécifie si l'ancre de la forme est verrouillée. |
| [get_AspectRatioLocked](./get_aspectratiolocked/)() | Spécifie si le ratio d'aspect de la forme est verrouillé. |
| [get_BehindText](./get_behindtext/)() | Spécifie si la forme est en dessous ou au-dessus du texte. |
| [get_Bottom](./get_bottom/)() | Obtient la position du bord inférieur du bloc contenant la forme. |
| [get_Bounds](./get_bounds/)() | Obtient ou définit l'emplacement et la taille du bloc contenant la forme. |
| [get_BoundsInPoints](./get_boundsinpoints/)() | Obtient l'emplacement et la taille du bloc contenant la forme en points, par rapport à l'ancre de la forme la plus haute. |
| [get_BoundsWithEffects](./get_boundswitheffects/)() | Obtient l'étendue finale que cet objet forme possède après l'application des effets de dessin. La valeur est mesurée en points. |
| [get_CanHaveImage](./get_canhaveimage/)() | Renvoie **true** si le type de forme autorise la forme à contenir une image. |
| [get_CoordOrigin](./get_coordorigin/)() | Les coordonnées du coin supérieur gauche du bloc contenant cette forme. |
| [get_CoordSize](./get_coordsize/)() | La largeur et la hauteur de l'espace de coordonnées à l'intérieur du bloc contenant cette forme. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Obtient le nombre d'enfants immédiats de ce nœud. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Spécifie un identifiant de nœud personnalisé. |
| [get_DistanceBottom](./get_distancebottom/)() | Renvoie ou définit la distance (en points) entre le texte du document et le bord inférieur de la forme. |
| [get_DistanceLeft](./get_distanceleft/)() | Renvoie ou définit la distance (en points) entre le texte du document et le bord gauche de la forme. |
| [get_DistanceRight](./get_distanceright/)() | Renvoie ou définit la distance (en points) entre le texte du document et le bord droit de la forme. |
| [get_DistanceTop](./get_distancetop/)() | Renvoie ou définit la distance (en points) entre le texte du document et le bord supérieur de la forme. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Obtient le document auquel ce nœud appartient. |
| [get_Fill](./get_fill/)() | Obtient le format de remplissage de la forme. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Obtient le premier enfant du nœud. |
| [get_FlipOrientation](./get_fliporientation/)() | Change l'orientation d'une forme. |
| [get_Font](./get_font/)() | Fournit l'accès au format de police de cet objet. |
| [get_Glow](./get_glow/)() | Obtient le format de lueur de la forme. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Renvoie **true** si ce nœud possède des nœuds enfants. |
| [get_Height](./get_height/)() | Obtient ou définit la hauteur du bloc contenant la forme. |
| [get_HeightRelative](./get_heightrelative/)() | Obtient ou définit la valeur qui représente le pourcentage de la hauteur relative de la forme. |
| [get_Hidden](./get_hidden/)() | Obtient ou définit une valeur booléenne indiquant si la forme est visible. |
| [get_HorizontalAlignment](./get_horizontalalignment/)() | Spécifie comment la forme est positionnée horizontalement. |
| [get_HRef](./get_href/)() | Obtient ou définit l'adresse complète du lien hypertexte pour une forme. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Renvoie **true** car ce nœud peut avoir des nœuds enfants. |
| [get_IsDecorative](./get_isdecorative/)() | Obtient ou définit le drapeau qui indique si la forme est décorative dans le document. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Renvoie true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsGroup](./get_isgroup/)() | Renvoie **true** si c'est une forme de groupe. |
| [get_IsHorizontalRule](./get_ishorizontalrule/)() | Renvoie **true** si cette forme est une règle horizontale. |
| [get_IsImage](./get_isimage/)() | Renvoie **true** si cette forme est une forme d'image. |
| [get_IsInline](./get_isinline/)() | Un moyen rapide de déterminer si cette forme est positionnée en ligne avec le texte. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Renvoie true si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsLayoutInCell](./get_islayoutincell/)() | Obtient ou définit un drapeau indiquant si la forme est affichée à l'intérieur d'un tableau ou en dehors de celui-ci. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Renvoie **true** si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Renvoie **true** si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsSignatureLine](./get_issignatureline/)() | Indique que la forme est une [SignatureLine](../signatureline/). |
| [get_IsTopLevel](./get_istoplevel/)() | Renvoie **true** si cette forme n'est pas un enfant d'une forme de groupe. |
| [get_IsWordArt](./get_iswordart/)() | Renvoie **true** si cette forme est un objet WordArt. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Obtient le dernier enfant du nœud. |
| [get_Left](./get_left/)() | Obtient ou définit la position du bord gauche du bloc contenant de la forme. |
| [get_LeftRelative](./get_leftrelative/)() | Obtient ou définit la valeur qui représente la position gauche relative de la forme en pourcentage. |
| [get_MarkupLanguage](./get_markuplanguage/)() const | Obtient le MarkupLanguage utilisé pour cet objet graphique. |
| [get_Name](./get_name/)() | Obtient ou définit le nom optionnel de la forme. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Obtient le nœud immédiatement suivant ce nœud. |
| virtual [get_NodeType](../../aspose.words/node/get_nodetype/)() const | Obtient le type de ce nœud. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Obtient le parent immédiat de ce nœud. |
| [get_ParentParagraph](./get_parentparagraph/)() | Renvoie le paragraphe parent immédiat. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Obtient le nœud immédiatement précédent ce nœud. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Renvoie un objet [Range](../../aspose.words/range/) qui représente la partie d'un document contenue dans ce nœud. |
| [get_Reflection](./get_reflection/)() | Obtient le formatage de réflexion pour la forme. |
| [get_RelativeHorizontalPosition](./get_relativehorizontalposition/)() | Spécifie par rapport à quoi la forme est positionnée horizontalement. |
| [get_RelativeHorizontalSize](./get_relativehorizontalsize/)() | Obtient ou définit la valeur de la taille relative de la forme dans la direction horizontale. |
| [get_RelativeVerticalPosition](./get_relativeverticalposition/)() | Spécifie par rapport à quoi la forme est positionnée verticalement. |
| [get_RelativeVerticalSize](./get_relativeverticalsize/)() | Obtient ou définit la valeur de la taille relative de la forme dans la direction verticale. |
| [get_Right](./get_right/)() | Obtient la position du bord droit du bloc contenant de la forme. |
| [get_Rotation](./get_rotation/)() | Définit l'angle (en degrés) auquel une forme est tournée. Une valeur positive correspond à un angle de rotation horaire. |
| [get_ScreenTip](./get_screentip/)() | Définit le texte affiché lorsque le pointeur de la souris survole la forme. |
| [get_ShadowFormat](./get_shadowformat/)() | Obtient le format d'ombre pour la forme. |
| [get_ShapeType](./get_shapetype/)() | Obtient le type de forme. |
| [get_SizeInPoints](./get_sizeinpoints/)() | Obtient la taille de la forme en points. |
| [get_SoftEdge](./get_softedge/)() | Obtient le format de bord doux pour la forme. |
| [get_Target](./get_target/)() | Obtient ou définit le cadre cible pour le lien hypertexte de la forme. |
| [get_Title](./get_title/)() | Obtient ou définit le titre (légende) de l'objet forme actuel. |
| [get_Top](./get_top/)() | Obtient ou définit la position du bord supérieur du bloc contenant de la forme. |
| [get_TopRelative](./get_toprelative/)() | Obtient ou définit la valeur qui représente la position supérieure relative de la forme en pourcentage. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Spécifie comment la forme est positionnée verticalement. |
| [get_Width](./get_width/)() | Obtient ou définit la largeur du bloc contenant de la forme. |
| [get_WidthRelative](./get_widthrelative/)() | Obtient ou définit la valeur qui représente le pourcentage de la largeur relative de la forme. |
| [get_WrapSide](./get_wrapside/)() | Spécifie comment le texte s'enroule autour de la forme. |
| [get_WrapType](./get_wraptype/)() | Définit si la forme est en ligne ou flottante. Pour les formes flottantes, définit le mode d'habillage du texte autour de la forme. |
| [get_ZOrder](./get_zorder/)() | Détermine l'ordre d'affichage des formes qui se chevauchent. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Obtient le premier ancêtre du [NodeType](../../aspose.words/nodetype/) spécifié. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Renvoie le nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Renvoie une collection dynamique de nœuds enfants qui correspondent au type spécifié. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Fournit une prise en charge de l'itération de type foreach sur les nœuds enfants de ce nœud. |
| [GetShapeRenderer](./getshaperenderer/)() | Crée et renvoie un objet pouvant être utilisé pour rendre cette forme en image. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Obtient le texte de ce nœud et de tous ses enfants. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Renvoie l'index du nœud enfant spécifié dans le tableau des nœuds enfants. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [LocalToParent](./localtoparent/)(System::Drawing::PointF) | Convertit une valeur de l'espace de coordonnées local vers l'espace de coordonnées de la forme parent. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud suivant selon l'algorithme de traversée d'arbre en pré-ordre. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Méthode utilitaire qui convertit une valeur d'énumération de type de nœud en une chaîne conviviale. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud précédent selon l'algorithme de traversée d'arbre en pré-ordre. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Supprime tous les nœuds descendants [SmartTag](../../aspose.words.markup/smarttag/) du nœud actuel. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Sélectionne le premier [Node](../../aspose.words/node/) qui correspond à l'expression XPath. |
| [set_AllowOverlap](./set_allowoverlap/)(bool) | Mutateur pour [Aspose::Words::Drawing::ShapeBase::get_AllowOverlap](./get_allowoverlap/). |
| [set_AlternativeText](./set_alternativetext/)(const System::String\&) | Mutateur pour [Aspose::Words::Drawing::ShapeBase::get_AlternativeText](./get_alternativetext/). |
| [set_AnchorLocked](./set_anchorlocked/)(bool) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_AnchorLocked](./get_anchorlocked/). |
| [set_AspectRatioLocked](./set_aspectratiolocked/)(bool) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked](./get_aspectratiolocked/). |
| [set_BehindText](./set_behindtext/)(bool) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_BehindText](./get_behindtext/). |
| [set_Bounds](./set_bounds/)(System::Drawing::RectangleF) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_Bounds](./get_bounds/). |
| [set_CoordOrigin](./set_coordorigin/)(System::Drawing::Point) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_CoordOrigin](./get_coordorigin/). |
| [set_CoordSize](./set_coordsize/)(System::Drawing::Size) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_CoordSize](./get_coordsize/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Mutateur pour [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DistanceBottom](./set_distancebottom/)(double) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_DistanceBottom](./get_distancebottom/). |
| [set_DistanceLeft](./set_distanceleft/)(double) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_DistanceLeft](./get_distanceleft/). |
| [set_DistanceRight](./set_distanceright/)(double) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_DistanceRight](./get_distanceright/). |
| [set_DistanceTop](./set_distancetop/)(double) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_DistanceTop](./get_distancetop/). |
| [set_FlipOrientation](./set_fliporientation/)(Aspose::Words::Drawing::FlipOrientation) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_FlipOrientation](./get_fliporientation/). |
| [set_Height](./set_height/)(double) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_Height](./get_height/). |
| [set_HeightRelative](./set_heightrelative/)(float) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_HeightRelative](./get_heightrelative/). |
| [set_Hidden](./set_hidden/)(bool) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_Hidden](./get_hidden/). |
| [set_HorizontalAlignment](./set_horizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment](./get_horizontalalignment/). |
| [set_HRef](./set_href/)(const System::String\&) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_HRef](./get_href/). |
| [set_IsDecorative](./set_isdecorative/)(bool) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_IsDecorative](./get_isdecorative/). |
| [set_IsLayoutInCell](./set_islayoutincell/)(bool) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell](./get_islayoutincell/). |
| [set_Left](./set_left/)(double) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_Left](./get_left/). |
| [set_LeftRelative](./set_leftrelative/)(float) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_LeftRelative](./get_leftrelative/). |
| [set_Name](./set_name/)(const System::String\&) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_Name](./get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalPosition](./set_relativehorizontalposition/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition](./get_relativehorizontalposition/). |
| [set_RelativeHorizontalSize](./set_relativehorizontalsize/)(Aspose::Words::Drawing::RelativeHorizontalSize) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize](./get_relativehorizontalsize/). |
| [set_RelativeVerticalPosition](./set_relativeverticalposition/)(Aspose::Words::Drawing::RelativeVerticalPosition) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition](./get_relativeverticalposition/). |
| [set_RelativeVerticalSize](./set_relativeverticalsize/)(Aspose::Words::Drawing::RelativeVerticalSize) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize](./get_relativeverticalsize/). |
| [set_Rotation](./set_rotation/)(double) | Définisseur de [Aspose::Words::Drawing::ShapeBase::get_Rotation](./get_rotation/). |
| [set_ScreenTip](./set_screentip/)(const System::String\&) | Définisseur de [Aspose::Words::Drawing::ShapeBase::get_ScreenTip](./get_screentip/). |
| [set_Target](./set_target/)(const System::String\&) | Définisseur de [Aspose::Words::Drawing::ShapeBase::get_Target](./get_target/). |
| [set_Title](./set_title/)(const System::String\&) | Définisseur de [Aspose::Words::Drawing::ShapeBase::get_Title](./get_title/). |
| [set_Top](./set_top/)(double) | Définisseur de [Aspose::Words::Drawing::ShapeBase::get_Top](./get_top/). |
| [set_TopRelative](./set_toprelative/)(float) | Définisseur de [Aspose::Words::Drawing::ShapeBase::get_TopRelative](./get_toprelative/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | Définisseur de [Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment](./get_verticalalignment/). |
| [set_Width](./set_width/)(double) | Définisseur de [Aspose::Words::Drawing::ShapeBase::get_Width](./get_width/). |
| [set_WidthRelative](./set_widthrelative/)(float) | Définisseur de [Aspose::Words::Drawing::ShapeBase::get_WidthRelative](./get_widthrelative/). |
| [set_WrapSide](./set_wrapside/)(Aspose::Words::Drawing::WrapSide) | Définisseur de [Aspose::Words::Drawing::ShapeBase::get_WrapSide](./get_wrapside/). |
| [set_WrapType](./set_wraptype/)(Aspose::Words::Drawing::WrapType) | Définisseur de [Aspose::Words::Drawing::ShapeBase::get_WrapType](./get_wraptype/). |
| [set_ZOrder](./set_zorder/)(int32_t) | Définisseur de [Aspose::Words::Drawing::ShapeBase::get_ZOrder](./get_zorder/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporte le contenu du nœud dans une chaîne en utilisant les options d'enregistrement spécifiées. |
| static [Type](./type/)() |  |
## Remarques


Ceci est une classe abstraite. Les deux classes dérivées que vous pouvez instancier sont [Shape](../shape/) et [GroupShape](../groupshape/).

Une forme est un nœud dans l'arbre du document.

Si la forme est un enfant d'un objet [Paragraph](../../aspose.words/paragraph/), alors on dit que la forme est « de niveau supérieur ». Les formes de niveau supérieur sont mesurées et positionnées en points.

Une forme peut également apparaître comme enfant d'un objet [GroupShape](../groupshape/) lorsque plusieurs formes sont groupées. Les formes enfants d'un groupe sont positionnées dans l'espace de coordonnées et les unités définies par les propriétés [CoordSize](./get_coordsize/) et [CoordOrigin](./get_coordorigin/) du groupe parent.

Une forme peut être positionnée en ligne avec le texte ou en flottant. La méthode de positionnement est contrôlée à l'aide de la propriété [WrapType](./get_wraptype/).

Lorsqu'une forme flotte, elle est positionnée par rapport à quelque chose (par ex. le paragraphe actuel, la marge ou la page). Le positionnement relatif de la forme est spécifié à l'aide des propriétés [RelativeHorizontalPosition](./get_relativehorizontalposition/) et [RelativeVerticalPosition](./get_relativeverticalposition/).

Une forme flottante peut être positionnée explicitement à l'aide des propriétés [Left](./get_left/) et [Top](./get_top/) ou alignée relativement à un autre objet à l'aide des propriétés [HorizontalAlignment](./get_horizontalalignment/) et [VerticalAlignment](./get_verticalalignment/).

## Exemples



Montre comment insérer une image flottante au centre d'une page.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez une image flottante qui apparaîtra derrière le texte qui se chevauche et alignez‑la au centre de la page.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## Voir aussi

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
