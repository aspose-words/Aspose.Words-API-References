---
title: "Aspose::Words::Section classe"
linktitle: "Section"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Section classe. Représente une seule section dans un document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 58000
url: /fr/cpp/aspose.words/section/
---
## Section class


Représente une section unique dans un document. Pour en savoir plus, consultez l'article de documentation [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class Section : public Aspose::Words::CompositeNode,
                public Aspose::Words::ISectionAttrSource
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Lorsqu'il est implémenté dans une classe dérivée, appelle la méthode VisitXXXEnd du visiteur de document spécifié. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Lorsqu'il est implémenté dans une classe dérivée, appelle la méthode VisitXXXStart du visiteur de document spécifié. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendContent](./appendcontent/)(const System::SharedPtr\<Aspose::Words::Section\>\&) | Insère une copie du contenu de la section source à la fin de cette section. |
| [ClearContent](./clearcontent/)() | Efface la section. |
| [ClearHeadersFooters](./clearheadersfooters/)() | Efface les en-têtes et pieds de page de cette section. |
| [ClearHeadersFooters](./clearheadersfooters/)(bool) | Efface les en-têtes et pieds de page de cette section. |
| [Clone](./clone/)() | Crée un duplicata de cette section. |
| [Clone](../node/clone/)(bool) | Crée un duplicata du nœud. |
| [DeleteHeaderFooterShapes](./deleteheaderfootershapes/)() | Supprime toutes les formes (objets de dessin) des en-têtes et pieds de page de cette section. |
| [EnsureMinimum](./ensureminimum/)() | Assure que la section possède un [Body](./get_body/) avec un [Paragraph](../paragraph/). |
| [get_Body](./get_body/)() | Renvoie le nœud enfant [Body](../body/) de la section. |
| [get_Count](../compositenode/get_count/)() | Obtient le nombre d'enfants immédiats de ce nœud. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Spécifie un identifiant de nœud personnalisé. |
| virtual [get_Document](../node/get_document/)() const | Obtient le document auquel ce nœud appartient. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Obtient le premier enfant du nœud. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Renvoie **true** si ce nœud possède des nœuds enfants. |
| [get_HeadersFooters](./get_headersfooters/)() | Fournit l'accès aux nœuds des en-têtes et pieds de page de la section. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Renvoie **true** car ce nœud peut avoir des nœuds enfants. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Obtient le dernier enfant du nœud. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Obtient le nœud immédiatement suivant ce nœud. |
| [get_NodeType](./get_nodetype/)() const override | Renvoie [Section](../nodetype/). |
| [get_PageSetup](./get_pagesetup/)() | Renvoie un objet qui représente la configuration de la page et les propriétés de la section. |
| [get_ParentNode](../node/get_parentnode/)() | Obtient le parent immédiat de ce nœud. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Obtient le nœud immédiatement précédent ce nœud. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_ProtectedForForms](./get_protectedforforms/)() | Vrai si la section est protégée pour les formulaires. Lorsqu'une section est protégée pour les formulaires, les utilisateurs ne peuvent sélectionner et modifier le texte que dans les champs de formulaire dans Microsoft Word. |
| [get_Range](../node/get_range/)() | Renvoie un objet [Range](../range/) qui représente la partie d'un document contenue dans ce nœud. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Obtient le premier ancêtre du [NodeType](../nodetype/) spécifié. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Renvoie le nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Renvoie une collection dynamique de nœuds enfants qui correspondent au type spécifié. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Fournit une prise en charge de l'itération de type foreach sur les nœuds enfants de ce nœud. |
| [GetText](../compositenode/gettext/)() override | Obtient le texte de ce nœud et de tous ses enfants. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Renvoie l'index du nœud enfant spécifié dans le tableau des nœuds enfants. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud suivant selon l'algorithme de traversée d'arbre en pré-ordre. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Méthode utilitaire qui convertit une valeur d'énumération de type de nœud en une chaîne conviviale. |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PrependContent](./prependcontent/)(const System::SharedPtr\<Aspose::Words::Section\>\&) | Insère une copie du contenu de la section source au début de cette section. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud précédent selon l'algorithme de traversée d'arbre en pré-ordre. |
| [Remove](../node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Supprime tous les nœuds descendants [SmartTag](../../aspose.words.markup/smarttag/) du nœud actuel. |
| [Section](./section/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Initialise une nouvelle instance de la classe [Section](./). |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Sélectionne le premier [Node](../node/) qui correspond à l'expression XPath. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Définisseur pour [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ProtectedForForms](./set_protectedforforms/)(bool) | Définisseur pour [Aspose::Words::Section::get_ProtectedForForms](./get_protectedforforms/). |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporte le contenu du nœud dans une chaîne en utilisant les options d'enregistrement spécifiées. |
| static [Type](./type/)() |  |
## Remarques


[Section](./) can have one [Body](../body/) and maximum one [HeaderFooter](../headerfooter/) of each [HeaderFooterType](../headerfootertype/). [Body](../body/) and [HeaderFooter](../headerfooter/) nodes can be in any order inside [Section](./).

Une section minimale valide doit contenir un [Body](../body/) avec un [Paragraph](../paragraph/).

Chaque section possède son propre ensemble de propriétés qui spécifient la taille de la page, l'orientation, les marges, etc.

Vous pouvez créer une copie d'une section en utilisant [Clone()](../node/clone/). La copie peut être insérée dans le même document ou dans un document différent.

Pour ajouter, insérer ou supprimer une section entière, y compris le saut de section et les propriétés de section, utilisez les méthodes de l'objet [Sections](../document/get_sections/).

Pour copier et insérer uniquement le contenu de la section en excluant le saut de section et les propriétés de section, utilisez les méthodes [AppendContent()](../) et [PrependContent()](../).

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
