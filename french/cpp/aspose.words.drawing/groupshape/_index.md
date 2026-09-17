---
title: "Aspose::Words::Drawing::GroupShape class"
linktitle: "GroupShape"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::GroupShape classe. Représente un groupe de formes dans un document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.drawing/groupshape/
---
## GroupShape class


Représente un groupe de formes dans un document. Pour en savoir plus, consultez l'article de documentation [How to Add Group Shape into a Word Document](https://docs.aspose.com/words/cpp/how-to-add-group-shape-into-a-word-document/).

```cpp
class GroupShape : public Aspose::Words::Drawing::ShapeBase
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur pour visiter la fin du [GroupShape](./). |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur pour visiter le début du [GroupShape](./). |
| [AdjustWithEffects](../shapebase/adjustwitheffects/)(System::Drawing::RectangleF) | Ajoute aux valeurs du rectangle source l'étendue de l'effet et renvoie le rectangle final. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un duplicata du nœud. |
| [get_AllowOverlap](../shapebase/get_allowoverlap/)() | Obtient ou définit une valeur qui indique si cette forme peut chevaucher d'autres formes. |
| [get_AlternativeText](../shapebase/get_alternativetext/)() | Définit le texte alternatif à afficher à la place d'un graphique. |
| [get_AnchorLocked](../shapebase/get_anchorlocked/)() | Spécifie si l'ancre de la forme est verrouillée. |
| [get_AspectRatioLocked](../shapebase/get_aspectratiolocked/)() | Spécifie si le ratio d'aspect de la forme est verrouillé. |
| [get_BehindText](../shapebase/get_behindtext/)() | Spécifie si la forme est en dessous ou au-dessus du texte. |
| [get_Bottom](../shapebase/get_bottom/)() | Obtient la position du bord inférieur du bloc contenant la forme. |
| [get_Bounds](../shapebase/get_bounds/)() | Obtient ou définit l'emplacement et la taille du bloc contenant la forme. |
| [get_BoundsInPoints](../shapebase/get_boundsinpoints/)() | Obtient l'emplacement et la taille du bloc contenant la forme en points, par rapport à l'ancre de la forme la plus haute. |
| [get_BoundsWithEffects](../shapebase/get_boundswitheffects/)() | Obtient l'étendue finale que cet objet forme possède après l'application des effets de dessin. La valeur est mesurée en points. |
| [get_CanHaveImage](../shapebase/get_canhaveimage/)() | Renvoie **true** si le type de forme autorise la forme à contenir une image. |
| [get_CoordOrigin](../shapebase/get_coordorigin/)() | Les coordonnées du coin supérieur gauche du bloc contenant cette forme. |
| [get_CoordSize](../shapebase/get_coordsize/)() | La largeur et la hauteur de l'espace de coordonnées à l'intérieur du bloc contenant cette forme. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Obtient le nombre d'enfants immédiats de ce nœud. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Spécifie un identifiant de nœud personnalisé. |
| [get_DistanceBottom](../shapebase/get_distancebottom/)() | Renvoie ou définit la distance (en points) entre le texte du document et le bord inférieur de la forme. |
| [get_DistanceLeft](../shapebase/get_distanceleft/)() | Renvoie ou définit la distance (en points) entre le texte du document et le bord gauche de la forme. |
| [get_DistanceRight](../shapebase/get_distanceright/)() | Renvoie ou définit la distance (en points) entre le texte du document et le bord droit de la forme. |
| [get_DistanceTop](../shapebase/get_distancetop/)() | Renvoie ou définit la distance (en points) entre le texte du document et le bord supérieur de la forme. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Obtient le document auquel ce nœud appartient. |
| [get_Fill](../shapebase/get_fill/)() | Obtient le format de remplissage de la forme. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Obtient le premier enfant du nœud. |
| [get_FlipOrientation](../shapebase/get_fliporientation/)() | Change l'orientation d'une forme. |
| [get_Font](../shapebase/get_font/)() | Fournit l'accès au format de police de cet objet. |
| [get_Glow](../shapebase/get_glow/)() | Obtient le format de lueur de la forme. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Renvoie **true** si ce nœud possède des nœuds enfants. |
| [get_Height](../shapebase/get_height/)() | Obtient ou définit la hauteur du bloc contenant la forme. |
| [get_HeightRelative](../shapebase/get_heightrelative/)() | Obtient ou définit la valeur qui représente le pourcentage de la hauteur relative de la forme. |
| [get_Hidden](../shapebase/get_hidden/)() | Obtient ou définit une valeur booléenne indiquant si la forme est visible. |
| [get_HorizontalAlignment](../shapebase/get_horizontalalignment/)() | Spécifie comment la forme est positionnée horizontalement. |
| [get_HRef](../shapebase/get_href/)() | Obtient ou définit l'adresse complète du lien hypertexte pour une forme. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Renvoie **true** car ce nœud peut avoir des nœuds enfants. |
| [get_IsDecorative](../shapebase/get_isdecorative/)() | Obtient ou définit le drapeau qui indique si la forme est décorative dans le document. |
| [get_IsDeleteRevision](../shapebase/get_isdeleterevision/)() | Renvoie true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsGroup](../shapebase/get_isgroup/)() | Renvoie **true** si c'est une forme de groupe. |
| [get_IsHorizontalRule](../shapebase/get_ishorizontalrule/)() | Renvoie **true** si cette forme est une règle horizontale. |
| [get_IsImage](../shapebase/get_isimage/)() | Renvoie **true** si cette forme est une forme d'image. |
| [get_IsInline](../shapebase/get_isinline/)() | Un moyen rapide de déterminer si cette forme est positionnée en ligne avec le texte. |
| [get_IsInsertRevision](../shapebase/get_isinsertrevision/)() | Renvoie true si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsLayoutInCell](../shapebase/get_islayoutincell/)() | Obtient ou définit un drapeau indiquant si la forme est affichée à l'intérieur d'un tableau ou en dehors de celui-ci. |
| [get_IsMoveFromRevision](../shapebase/get_ismovefromrevision/)() | Renvoie **true** si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsMoveToRevision](../shapebase/get_ismovetorevision/)() | Renvoie **true** si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsSignatureLine](../shapebase/get_issignatureline/)() | Indique que la forme est une [SignatureLine](../signatureline/). |
| [get_IsTopLevel](../shapebase/get_istoplevel/)() | Renvoie **true** si cette forme n'est pas un enfant d'une forme de groupe. |
| [get_IsWordArt](../shapebase/get_iswordart/)() | Renvoie **true** si cette forme est un objet WordArt. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Obtient le dernier enfant du nœud. |
| [get_Left](../shapebase/get_left/)() | Obtient ou définit la position du bord gauche du bloc contenant de la forme. |
| [get_LeftRelative](../shapebase/get_leftrelative/)() | Obtient ou définit la valeur qui représente la position gauche relative de la forme en pourcentage. |
| [get_MarkupLanguage](../shapebase/get_markuplanguage/)() const | Obtient le MarkupLanguage utilisé pour cet objet graphique. |
| [get_Name](../shapebase/get_name/)() | Obtient ou définit le nom optionnel de la forme. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Obtient le nœud immédiatement suivant ce nœud. |
| [get_NodeType](./get_nodetype/)() const override | Renvoie [GroupShape](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Obtient le parent immédiat de ce nœud. |
| [get_ParentParagraph](../shapebase/get_parentparagraph/)() | Renvoie le paragraphe parent immédiat. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Obtient le nœud immédiatement précédent ce nœud. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Renvoie un objet [Range](../../aspose.words/range/) qui représente la partie d'un document contenue dans ce nœud. |
| [get_Reflection](../shapebase/get_reflection/)() | Obtient le formatage de réflexion pour la forme. |
| [get_RelativeHorizontalPosition](../shapebase/get_relativehorizontalposition/)() | Spécifie par rapport à quoi la forme est positionnée horizontalement. |
| [get_RelativeHorizontalSize](../shapebase/get_relativehorizontalsize/)() | Obtient ou définit la valeur de la taille relative de la forme dans la direction horizontale. |
| [get_RelativeVerticalPosition](../shapebase/get_relativeverticalposition/)() | Spécifie par rapport à quoi la forme est positionnée verticalement. |
| [get_RelativeVerticalSize](../shapebase/get_relativeverticalsize/)() | Obtient ou définit la valeur de la taille relative de la forme dans la direction verticale. |
| [get_Right](../shapebase/get_right/)() | Obtient la position du bord droit du bloc contenant de la forme. |
| [get_Rotation](../shapebase/get_rotation/)() | Définit l'angle (en degrés) auquel une forme est tournée. Une valeur positive correspond à un angle de rotation horaire. |
| [get_ScreenTip](../shapebase/get_screentip/)() | Définit le texte affiché lorsque le pointeur de la souris survole la forme. |
| [get_ShadowFormat](../shapebase/get_shadowformat/)() | Obtient le format d'ombre pour la forme. |
| [get_ShapeType](../shapebase/get_shapetype/)() | Obtient le type de forme. |
| [get_SizeInPoints](../shapebase/get_sizeinpoints/)() | Obtient la taille de la forme en points. |
| [get_SoftEdge](../shapebase/get_softedge/)() | Obtient le format de bord doux pour la forme. |
| [get_Target](../shapebase/get_target/)() | Obtient ou définit le cadre cible pour le lien hypertexte de la forme. |
| [get_Title](../shapebase/get_title/)() | Obtient ou définit le titre (légende) de l'objet forme actuel. |
| [get_Top](../shapebase/get_top/)() | Obtient ou définit la position du bord supérieur du bloc contenant de la forme. |
| [get_TopRelative](../shapebase/get_toprelative/)() | Obtient ou définit la valeur qui représente la position supérieure relative de la forme en pourcentage. |
| [get_VerticalAlignment](../shapebase/get_verticalalignment/)() | Spécifie comment la forme est positionnée verticalement. |
| [get_Width](../shapebase/get_width/)() | Obtient ou définit la largeur du bloc contenant de la forme. |
| [get_WidthRelative](../shapebase/get_widthrelative/)() | Obtient ou définit la valeur qui représente le pourcentage de la largeur relative de la forme. |
| [get_WrapSide](../shapebase/get_wrapside/)() | Spécifie comment le texte s'enroule autour de la forme. |
| [get_WrapType](../shapebase/get_wraptype/)() | Définit si la forme est en ligne ou flottante. Pour les formes flottantes, définit le mode d'habillage du texte autour de la forme. |
| [get_ZOrder](../shapebase/get_zorder/)() | Détermine l'ordre d'affichage des formes qui se chevauchent. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Obtient le premier ancêtre du [NodeType](../../aspose.words/nodetype/) spécifié. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Renvoie le nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Renvoie une collection dynamique de nœuds enfants qui correspondent au type spécifié. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Fournit une prise en charge de l'itération de type foreach sur les nœuds enfants de ce nœud. |
| [GetShapeRenderer](../shapebase/getshaperenderer/)() | Crée et renvoie un objet pouvant être utilisé pour rendre cette forme en image. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Obtient le texte de ce nœud et de tous ses enfants. |
| [GetType](./gettype/)() const override |  |
| [GroupShape](./groupshape/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Crée une nouvelle forme groupée. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Renvoie l'index du nœud enfant spécifié dans le tableau des nœuds enfants. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [LocalToParent](../shapebase/localtoparent/)(System::Drawing::PointF) | Convertit une valeur de l'espace de coordonnées local vers l'espace de coordonnées de la forme parent. |
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
| [set_AllowOverlap](../shapebase/set_allowoverlap/)(bool) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_AllowOverlap](../shapebase/get_allowoverlap/). |
| [set_AlternativeText](../shapebase/set_alternativetext/)(const System::String\&) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_AlternativeText](../shapebase/get_alternativetext/). |
| [set_AnchorLocked](../shapebase/set_anchorlocked/)(bool) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_AnchorLocked](../shapebase/get_anchorlocked/). |
| [set_AspectRatioLocked](../shapebase/set_aspectratiolocked/)(bool) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked](../shapebase/get_aspectratiolocked/). |
| [set_BehindText](../shapebase/set_behindtext/)(bool) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_BehindText](../shapebase/get_behindtext/). |
| [set_Bounds](../shapebase/set_bounds/)(System::Drawing::RectangleF) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_Bounds](../shapebase/get_bounds/). |
| [set_CoordOrigin](../shapebase/set_coordorigin/)(System::Drawing::Point) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_CoordOrigin](../shapebase/get_coordorigin/). |
| [set_CoordSize](../shapebase/set_coordsize/)(System::Drawing::Size) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_CoordSize](../shapebase/get_coordsize/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Mutateur pour [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DistanceBottom](../shapebase/set_distancebottom/)(double) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_DistanceBottom](../shapebase/get_distancebottom/). |
| [set_DistanceLeft](../shapebase/set_distanceleft/)(double) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_DistanceLeft](../shapebase/get_distanceleft/). |
| [set_DistanceRight](../shapebase/set_distanceright/)(double) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_DistanceRight](../shapebase/get_distanceright/). |
| [set_DistanceTop](../shapebase/set_distancetop/)(double) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_DistanceTop](../shapebase/get_distancetop/). |
| [set_FlipOrientation](../shapebase/set_fliporientation/)(Aspose::Words::Drawing::FlipOrientation) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_FlipOrientation](../shapebase/get_fliporientation/). |
| [set_Height](../shapebase/set_height/)(double) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_Height](../shapebase/get_height/). |
| [set_HeightRelative](../shapebase/set_heightrelative/)(float) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_HeightRelative](../shapebase/get_heightrelative/). |
| [set_Hidden](../shapebase/set_hidden/)(bool) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_Hidden](../shapebase/get_hidden/). |
| [set_HorizontalAlignment](../shapebase/set_horizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment](../shapebase/get_horizontalalignment/). |
| [set_HRef](../shapebase/set_href/)(const System::String\&) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_HRef](../shapebase/get_href/). |
| [set_IsDecorative](../shapebase/set_isdecorative/)(bool) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_IsDecorative](../shapebase/get_isdecorative/). |
| [set_IsLayoutInCell](../shapebase/set_islayoutincell/)(bool) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell](../shapebase/get_islayoutincell/). |
| [set_Left](../shapebase/set_left/)(double) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_Left](../shapebase/get_left/). |
| [set_LeftRelative](../shapebase/set_leftrelative/)(float) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_LeftRelative](../shapebase/get_leftrelative/). |
| [set_Name](../shapebase/set_name/)(const System::String\&) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_Name](../shapebase/get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalPosition](../shapebase/set_relativehorizontalposition/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition](../shapebase/get_relativehorizontalposition/). |
| [set_RelativeHorizontalSize](../shapebase/set_relativehorizontalsize/)(Aspose::Words::Drawing::RelativeHorizontalSize) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize](../shapebase/get_relativehorizontalsize/). |
| [set_RelativeVerticalPosition](../shapebase/set_relativeverticalposition/)(Aspose::Words::Drawing::RelativeVerticalPosition) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition](../shapebase/get_relativeverticalposition/). |
| [set_RelativeVerticalSize](../shapebase/set_relativeverticalsize/)(Aspose::Words::Drawing::RelativeVerticalSize) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize](../shapebase/get_relativeverticalsize/). |
| [set_Rotation](../shapebase/set_rotation/)(double) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_Rotation](../shapebase/get_rotation/). |
| [set_ScreenTip](../shapebase/set_screentip/)(const System::String\&) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_ScreenTip](../shapebase/get_screentip/). |
| [set_Target](../shapebase/set_target/)(const System::String\&) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_Target](../shapebase/get_target/). |
| [set_Title](../shapebase/set_title/)(const System::String\&) | Définisseur pour [Aspose::Words::Drawing::ShapeBase::get_Title](../shapebase/get_title/). |
| [set_Top](../shapebase/set_top/)(double) | Définisseur de [Aspose::Words::Drawing::ShapeBase::get_Top](../shapebase/get_top/). |
| [set_TopRelative](../shapebase/set_toprelative/)(float) | Définisseur de [Aspose::Words::Drawing::ShapeBase::get_TopRelative](../shapebase/get_toprelative/). |
| [set_VerticalAlignment](../shapebase/set_verticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | Définisseur de [Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment](../shapebase/get_verticalalignment/). |
| [set_Width](../shapebase/set_width/)(double) | Définisseur de [Aspose::Words::Drawing::ShapeBase::get_Width](../shapebase/get_width/). |
| [set_WidthRelative](../shapebase/set_widthrelative/)(float) | Définisseur de [Aspose::Words::Drawing::ShapeBase::get_WidthRelative](../shapebase/get_widthrelative/). |
| [set_WrapSide](../shapebase/set_wrapside/)(Aspose::Words::Drawing::WrapSide) | Définisseur de [Aspose::Words::Drawing::ShapeBase::get_WrapSide](../shapebase/get_wrapside/). |
| [set_WrapType](../shapebase/set_wraptype/)(Aspose::Words::Drawing::WrapType) | Définisseur de [Aspose::Words::Drawing::ShapeBase::get_WrapType](../shapebase/get_wraptype/). |
| [set_ZOrder](../shapebase/set_zorder/)(int32_t) | Définisseur de [Aspose::Words::Drawing::ShapeBase::get_ZOrder](../shapebase/get_zorder/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporte le contenu du nœud dans une chaîne en utilisant les options d'enregistrement spécifiées. |
| static [Type](./type/)() |  |
## Remarques


Un [GroupShape](./) est un nœud composite et peut contenir des nœuds [Shape](../shape/) et [GroupShape](./) comme enfants.

Chaque [GroupShape](./) définit un nouveau système de coordonnées pour ses formes enfants. Le système de coordonnées est défini à l'aide des propriétés [CoordSize](../shapebase/get_coordsize/) et [CoordOrigin](../shapebase/get_coordorigin/).

## Voir aussi

* Class [ShapeBase](../shapebase/)
* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
