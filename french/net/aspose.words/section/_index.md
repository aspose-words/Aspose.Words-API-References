---
title: Class Section
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Section classe. Représente une seule section dans un document.
type: docs
weight: 5440
url: /fr/net/aspose.words/section/
---
## Section class

Représente une seule section dans un document.

```csharp
public sealed class Section : CompositeNode
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [Section](section/)(DocumentBase) | Initialise une nouvelle instance de la classe Section. |

## Propriétés

| Nom | La description |
| --- | --- |
| [Body](../../aspose.words/section/body/) { get; } | Renvoie le **Corps** nœud enfant de la section. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Obtient tous les nœuds enfants immédiats de ce nœud. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtient le nombre d'enfants immédiats de ce nœud. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel ce nœud appartient. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtient le premier enfant du nœud. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Renvoie vrai si ce nœud a des nœuds enfants. |
| [HeadersFooters](../../aspose.words/section/headersfooters/) { get; } | Fournit l'accès aux nœuds d'en-têtes et de pieds de page de la section. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Renvoie true car ce nœud peut avoir des nœuds enfants. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtient le dernier enfant du nœud. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words/section/nodetype/) { get; } | Retours **NodeType.Section** . |
| [PageSetup](../../aspose.words/section/pagesetup/) { get; } | Renvoie un objet qui représente la mise en page et les propriétés de section. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [ProtectedForForms](../../aspose.words/section/protectedforforms/) { get; set; } | Vrai si la section est protégée pour les formulaires. Lorsqu'une section est protégée pour les formulaires, les utilisateurs peuvent sélectionner et modifier du texte uniquement dans les champs de formulaire de Microsoft Word. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un **Intervalle** objet qui représente la partie d'un document contenue dans ce nœud. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words/section/accept/)(DocumentVisitor) | Accepte un visiteur. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Ajoute le nœud spécifié à la fin de la liste des nœuds enfants pour ce nœud. |
| [AppendContent](../../aspose.words/section/appendcontent/)(Section) | Insère une copie du contenu de la section source à la fin de cette section. |
| [ClearContent](../../aspose.words/section/clearcontent/)() | Efface la section. |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters/)() | Efface les en-têtes et pieds de page de cette section. |
| [Clone](../../aspose.words/section/clone/#clone_1)() | Crée un doublon de cette section. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un doublon du nœud. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Réservé à l'utilisation du système. IXPathNavigable. |
| [DeleteHeaderFooterShapes](../../aspose.words/section/deleteheaderfootershapes/)() | Supprime toutes les formes (objets de dessin) des en-têtes et pieds de page de cette section. |
| [EnsureMinimum](../../aspose.words/section/ensureminimum/)() | S'assure que la section a un corps avec un paragraphe. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtient le premier ancêtre du spécifié[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtient le premier ancêtre du type d'objet spécifié. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Renvoie un Nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Renvoie une collection dynamique de nœuds enfants correspondant au type spécifié. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fournit la prise en charge de chaque itération de style sur les nœuds enfants de ce nœud. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Obtient le texte de ce nœud et de tous ses enfants. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Renvoie l'index du nœud enfant spécifié dans le tableau de nœuds enfants. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Insère le nœud spécifié immédiatement après le nœud de référence spécifié. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Insère le nœud spécifié juste avant le nœud de référence spécifié. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtient le nœud suivant selon l'algorithme de traversée de l'arbre de pré-ordre. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Ajoute le nœud spécifié au début de la liste des nœuds enfants pour ce nœud. |
| [PrependContent](../../aspose.words/section/prependcontent/)(Section) | Insère une copie du contenu de la section source au début de cette section. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtient le nœud précédent selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Supprime le nœud enfant spécifié. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Supprime tout[`SmartTag`](../../aspose.words.markup/smarttag/) nœuds descendants du nœud actuel. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Sélectionne le premier nœud qui correspond à l'expression XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporte le contenu du nœud dans une chaîne à l'aide des options d'enregistrement spécifiées. |

### Remarques

**Section** peut en avoir un[`Body`](./body/) et maximum un[`HeaderFooter`](../headerfooter/) de chaque[`HeaderFooterType`](../headerfootertype/) . **Corps** et **En-têtePied de page** nodes peut être dans n'importe quel ordre à l'intérieur **Section**.

Une section minimale valide doit avoir **Corps** avec une **Paragraphe**.

Chaque section a son propre ensemble de propriétés qui spécifient la taille de la page, l'orientation, les marges, etc.

Vous pouvez créer une copie d'une section à l'aide de[`Clone`](../node/clone/). La copie peut être insérée dans le même document ou un document différent.

Pour ajouter, insérer ou supprimer une section entière, y compris les propriétés de saut de section et de section , utilisez les méthodes de **Sections** objet.

Pour copier et insérer uniquement le contenu de la section à l'exclusion de la section break et des propriétés de section, utilisez **AjouterContenu** et **PréfixeContenu**méthodes.

### Exemples

Montre comment construire un document Aspose.Words à la main.

```csharp
Document doc = new Document();

// Un document vierge contient une section, un corps et un paragraphe.
// Appelez la méthode "RemoveAllChildren" pour supprimer tous ces nœuds,
// et se retrouver avec un nœud de document sans enfants.
doc.RemoveAllChildren();

// Ce document n'a plus de nœuds enfants composites auxquels nous pouvons ajouter du contenu.
// Si nous souhaitons l'éditer, nous devrons repeupler sa collection de nœuds.
// Tout d'abord, créez une nouvelle section, puis ajoutez-la en tant qu'enfant au nœud de document racine.
Section section = new Section(doc);
doc.AppendChild(section);

// Définit certaines propriétés de mise en page pour la section.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Une section a besoin d'un corps, qui contiendra et affichera tout son contenu
// sur la page entre l'en-tête et le pied de page de la section.
Body body = new Body(doc);
section.AppendChild(body);

// Crée un paragraphe, définit certaines propriétés de formatage, puis l'ajoute en tant qu'enfant au corps.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Enfin, ajoutez du contenu pour faire le document. Créer une course,
// définit son apparence et son contenu, puis l'ajoute en tant qu'enfant au paragraphe.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Voir également

* class [CompositeNode](../compositenode/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


