---
title: "Classe Aspose::Words::Paragraph"
linktitle: "Paragraph"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Paragraph. Représente un paragraphe de texte. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 47000
url: /fr/cpp/aspose.words/paragraph/
---
## Paragraph class


Représente un paragraphe de texte. Pour en savoir plus, consultez l'article de documentation [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/).

```cpp
class Paragraph : public Aspose::Words::CompositeNode,
                  public Aspose::Words::IParaAttrSource,
                  public Aspose::Words::IRunAttrSource,
                  public Aspose::Words::Revisions::ITrackableNode
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur pour visiter la fin du paragraphe du document. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur pour visiter le début du paragraphe du document. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendField](./appendfield/)(Aspose::Words::Fields::FieldType, bool) | Ajoute un champ à ce paragraphe. |
| [AppendField](./appendfield/)(const System::String\&) | Ajoute un champ à ce paragraphe. |
| [AppendField](./appendfield/)(const System::String\&, const System::String\&) | Ajoute un champ à ce paragraphe. |
| [Clone](../node/clone/)(bool) | Crée un duplicata du nœud. |
| [get_BreakIsStyleSeparator](./get_breakisstyleseparator/)() | Vrai si ce saut de paragraphe est un séparateur [Style](../style/). Un séparateur de style permet à un paragraphe de se composer de parties ayant des styles de paragraphe différents. |
| [get_Count](../compositenode/get_count/)() | Obtient le nombre d'enfants immédiats de ce nœud. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Spécifie un identifiant de nœud personnalisé. |
| virtual [get_Document](../node/get_document/)() const | Obtient le document auquel ce nœud appartient. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Obtient le premier enfant du nœud. |
| [get_FrameFormat](./get_frameformat/)() | Fournit l'accès aux propriétés de formatage du cadre. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Renvoie **true** si ce nœud possède des nœuds enfants. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Renvoie **true** car ce nœud peut avoir des nœuds enfants. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Renvoie true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsEndOfCell](./get_isendofcell/)() | Vrai si ce paragraphe est le dernier paragraphe d'une [Cell](../../aspose.words.tables/cell/); sinon, faux. |
| [get_IsEndOfDocument](./get_isendofdocument/)() | Vrai si ce paragraphe est le dernier paragraphe de la dernière section du document. |
| [get_IsEndOfHeaderFooter](./get_isendofheaderfooter/)() | Vrai si ce paragraphe est le dernier paragraphe de l'[HeaderFooter](../headerfooter/) (histoire principale du texte) d'une [Section](../section/); sinon, faux. |
| [get_IsEndOfSection](./get_isendofsection/)() | Vrai si ce paragraphe est le dernier paragraphe du [Body](../body/) (histoire principale du texte) d'une [Section](../section/); sinon, faux. |
| [get_IsFormatRevision](./get_isformatrevision/)() | Renvoie vrai si le format de l'objet a été modifié dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsInCell](./get_isincell/)() | Vrai si ce paragraphe est un enfant immédiat d'une [Cell](../../aspose.words.tables/cell/); sinon, faux. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Renvoie true si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsListItem](./get_islistitem/)() | Vrai lorsque le paragraphe est un élément d'une liste à puces ou numérotée dans la révision originale. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Renvoie **true** si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Renvoie **true** si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Obtient le dernier enfant du nœud. |
| [get_ListFormat](./get_listformat/)() | Fournit l'accès aux propriétés de formatage de la liste du paragraphe. |
| [get_ListLabel](./get_listlabel/)() | Obtient un objet [ListLabel](./get_listlabel/) qui fournit l'accès à la valeur de numérotation de la liste et au formatage pour ce paragraphe. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Obtient le nœud immédiatement suivant ce nœud. |
| [get_NodeType](./get_nodetype/)() const override | Renvoie [Paragraph](../nodetype/). |
| [get_ParagraphBreakFont](./get_paragraphbreakfont/)() | Fournit l'accès au formatage de police du caractère de saut de paragraphe. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Fournit l'accès aux propriétés de formatage du paragraphe. |
| [get_ParentNode](../node/get_parentnode/)() | Obtient le parent immédiat de ce nœud. |
| [get_ParentSection](./get_parentsection/)() | Récupère la [Section](../section/) parente du paragraphe. |
| [get_ParentStory](./get_parentstory/)() | Récupère l'histoire au niveau de la section parente qui peut être [Body](../body/) ou [HeaderFooter](../headerfooter/). |
| [get_PreviousSibling](../node/get_previoussibling/)() | Obtient le nœud immédiatement précédent ce nœud. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Renvoie un objet [Range](../range/) qui représente la partie d'un document contenue dans ce nœud. |
| [get_Runs](./get_runs/)() | Fournit l'accès à la collection typée des fragments de texte à l'intérieur du paragraphe. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Obtient le premier ancêtre du [NodeType](../nodetype/) spécifié. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Renvoie le nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Renvoie une collection dynamique de nœuds enfants qui correspondent au type spécifié. |
| [GetEffectiveTabStops](./geteffectivetabstops/)() | Renvoie un tableau de tous les tabulations appliquées à ce paragraphe, y compris celles appliquées indirectement par les styles ou les listes. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Fournit une prise en charge de l'itération de type foreach sur les nœuds enfants de ce nœud. |
| [GetText](./gettext/)() override | Obtient le texte de ce paragraphe, y compris le caractère de fin de paragraphe. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Renvoie l'index du nœud enfant spécifié dans le tableau des nœuds enfants. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertField](./insertfield/)(Aspose::Words::Fields::FieldType, bool, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Insère un champ dans ce paragraphe. |
| [InsertField](./insertfield/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Insère un champ dans ce paragraphe. |
| [InsertField](./insertfield/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Insère un champ dans ce paragraphe. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)() | Fusionne les segments avec le même formatage dans le paragraphe. |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)(const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\&) | Fusionne les segments avec le même formatage dans le paragraphe. |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud suivant selon l'algorithme de traversée d'arbre en pré-ordre. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Méthode utilitaire qui convertit une valeur d'énumération de type de nœud en une chaîne conviviale. |
| [Paragraph](./paragraph/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Initialise une nouvelle instance de la classe [Paragraph](./). |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud précédent selon l'algorithme de traversée d'arbre en pré-ordre. |
| [Remove](../node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Supprime tous les nœuds descendants [SmartTag](../../aspose.words.markup/smarttag/) du nœud actuel. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Sélectionne le premier [Node](../node/) qui correspond à l'expression XPath. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Définisseur pour [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporte le contenu du nœud dans une chaîne en utilisant les options d'enregistrement spécifiées. |
| static [Type](./type/)() |  |
## Remarques


[Paragraph](./) is a block-level node and can be a child of classes derived from [Story](../story/) or [InlineStory](../inlinestory/).

[Paragraph](./) can contain any number of inline-level nodes and bookmarks.

La liste complète des nœuds enfants pouvant se trouver à l'intérieur d'un paragraphe comprend [BookmarkStart](../bookmarkstart/), [BookmarkEnd](../bookmarkend/), [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/), [FormField](../../aspose.words.fields/formfield/), [Comment](../comment/), [Footnote](../../aspose.words.notes/footnote/), [Run](../run/), [SpecialChar](../specialchar/), [Shape](../../aspose.words.drawing/shape/), [GroupShape](../../aspose.words.drawing/groupshape/), [SmartTag](../../aspose.words.markup/smarttag/).

Un paragraphe valide dans Microsoft Word se termine toujours par un caractère de saut de paragraphe et un paragraphe valide minimal se compose uniquement d'un saut de paragraphe. La classe [Paragraph](./) ajoute automatiquement le caractère de saut de paragraphe approprié à la fin et ce caractère ne fait pas partie des nœuds enfants du [Paragraph](./), ainsi un [Paragraph](./) peut être vide.

N'incluez pas les caractères de fin de paragraphe [ParagraphBreak](../controlchar/paragraphbreak/) ou de fin de cellule [Cell](../controlchar/cell/) dans le texte du paragraphe, car cela pourrait rendre le paragraphe invalide lors de l'ouverture du document dans Microsoft Word.

## Exemples



Montre comment construire un document Aspose.Words à la main.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un document vierge contient une section, un corps et un paragraphe.
// Appelez la méthode "RemoveAllChildren" pour supprimer tous ces nœuds,
// et obtenez un nœud de document sans enfants.
doc->RemoveAllChildren();

// Ce document n’a maintenant aucun nœud enfant composite auquel nous puissions ajouter du contenu.
// Si nous souhaitons le modifier, nous devrons reconstituer sa collection de nœuds.
// Tout d’abord, créez une nouvelle section, puis ajoutez-la en tant qu’enfant au nœud racine du document.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Définissez quelques propriétés de mise en page pour la section.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Une section nécessite un corps, qui contiendra et affichera tout son contenu
// sur la page entre l’en-tête et le pied-de-page de la section.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Créez un paragraphe, définissez quelques propriétés de mise en forme, puis ajoutez‑le en tant qu’enfant au corps.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Enfin, ajoutez du contenu au document. Créez un run,
// définissez son apparence et son contenu, puis ajoutez‑le en tant qu’enfant au paragraphe.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## Voir aussi

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
