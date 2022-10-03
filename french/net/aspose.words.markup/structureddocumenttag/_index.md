---
title: StructuredDocumentTag
second_title: Référence de l'API Aspose.Words pour .NET
description: Représente une balise de document structurée SDT ou contrôle de contenu dans un document.
type: docs
weight: 3820
url: /fr/net/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class

Représente une balise de document structurée (SDT ou contrôle de contenu) dans un document.

```csharp
public class StructuredDocumentTag : CompositeNode, IStructuredDocumentTag
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [StructuredDocumentTag](structureddocumenttag/)(DocumentBase, SdtType, MarkupLevel) | Initialise une nouvelle instance du **Balise de document structurée** classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttag/appearance/) { get; set; } | Obtient/définit l'apparence d'une balise de document structuré. |
| [BuildingBlockCategory](../../aspose.words.markup/structureddocumenttag/buildingblockcategory/) { get; set; } | Spécifie la catégorie de bloc de construction pour ce **TDS** node. Ne peut pas être null. |
| [BuildingBlockGallery](../../aspose.words.markup/structureddocumenttag/buildingblockgallery/) { get; set; } | Spécifie le type de bloc de construction pour ce **TDS** . Ne peut pas être nul. |
| [CalendarType](../../aspose.words.markup/structureddocumenttag/calendartype/) { get; set; } | Spécifie le type de calendrier pour ce **TDS** . La valeur par défaut estDefault |
| [Checked](../../aspose.words.markup/structureddocumenttag/checked/) { get; set; } | Obtient/Définit l'état actuel de la case à cocher **TDS** . La valeur par défaut de cette propriété est false. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Obtient tous les nœuds enfants immédiats de ce nœud. |
| [Color](../../aspose.words.markup/structureddocumenttag/color/) { get; set; } | Obtient ou définit la couleur de la balise de document structuré. |
| [ContentsFont](../../aspose.words.markup/structureddocumenttag/contentsfont/) { get; } | Formatage de la police qui sera appliqué au texte saisi dans **TDS** . |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtient le nombre d'enfants immédiats de ce nœud. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| [DateDisplayFormat](../../aspose.words.markup/structureddocumenttag/datedisplayformat/) { get; set; } | Chaîne qui représente le format dans lequel les dates sont affichées. Ne peut pas être nul. Les dates pour l'anglais (US) sont "mm/dd/yyyy" |
| [DateDisplayLocale](../../aspose.words.markup/structureddocumenttag/datedisplaylocale/) { get; set; } | Permet de définir/obtenir le format de langue pour la date affichée dans ce **TDS** . |
| [DateStorageFormat](../../aspose.words.markup/structureddocumenttag/datestorageformat/) { get; set; } | Obtient/définit le format dans lequel la date d'une date SDT est stockée lorsque le **TDS** est lié à un nœud XML dans le magasin de données du document. La valeur par défaut estDateTime |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel ce nœud appartient. |
| [EndCharacterFont](../../aspose.words.markup/structureddocumenttag/endcharacterfont/) { get; } | Formatage de la police qui sera appliqué au dernier caractère du texte saisi dans **TDS** . |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtient le premier enfant du nœud. |
| [FullDate](../../aspose.words.markup/structureddocumenttag/fulldate/) { get; set; } | Spécifie la date et l'heure complètes saisies pour la dernière fois dans ce **TDS** . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Renvoie vrai si ce nœud a des nœuds enfants. |
| [Id](../../aspose.words.markup/structureddocumenttag/id/) { get; } | Spécifie un identifiant numérique persistant unique en lecture seule pour ce **TDS**. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Renvoie true car ce nœud peut avoir des nœuds enfants. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttag/isshowingplaceholdertext/) { get; set; } | Spécifie si le contenu de ce **TDS** doit être interprété comme contenant un espace réservé text (par opposition au contenu textuel normal dans le SDT). |
| [IsTemporary](../../aspose.words.markup/structureddocumenttag/istemporary/) { get; set; } | Spécifie si cela **TDS** doit être supprimé du document WordProcessingML lorsque son contenu est modifié. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtient le dernier enfant du nœud. |
| [Level](../../aspose.words.markup/structureddocumenttag/level/) { get; } | Obtient le niveau auquel cette **TDS** se produit dans l'arborescence du document. |
| [ListItems](../../aspose.words.markup/structureddocumenttag/listitems/) { get; } | Obtient[`SdtListItemCollection`](../sdtlistitemcollection/) associé à ce **TDS** . |
| [LockContentControl](../../aspose.words.markup/structureddocumenttag/lockcontentcontrol/) { get; set; } | Lorsqu'elle est définie sur true, cette propriété interdit à un utilisateur de supprimer ce **TDS** . |
| [LockContents](../../aspose.words.markup/structureddocumenttag/lockcontents/) { get; set; } | Lorsqu'elle est définie sur true, cette propriété interdit à un utilisateur de modifier le contenu de ce **TDS** . |
| [Multiline](../../aspose.words.markup/structureddocumenttag/multiline/) { get; set; } | Spécifie si cela **TDS** autorise plusieurs lignes de texte. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words.markup/structureddocumenttag/nodetype/) { get; } | Retours **NodeType.StructuredDocumentTag** . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [Placeholder](../../aspose.words.markup/structureddocumenttag/placeholder/) { get; } | Obtient le[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) contenant un texte d'espace réservé qui doit être affiché lorsque le contenu de cette exécution SDT est vide, l'élément XML mappé associé est vide comme spécifié via le[`XmlMapping`](./xmlmapping/) element ou le[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) l'élément est vrai. |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttag/placeholdername/) { get; set; } | Obtient ou définit le nom du[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) contenant du texte d'espace réservé. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un **Intervalle** objet qui représente la partie d'un document contenue dans ce nœud. |
| [SdtType](../../aspose.words.markup/structureddocumenttag/sdttype/) { get; } | Obtient le type de ceci **Balise de document structurée** . |
| [Style](../../aspose.words.markup/structureddocumenttag/style/) { get; set; } | Obtient ou définit le style de la balise de document structuré. |
| [StyleName](../../aspose.words.markup/structureddocumenttag/stylename/) { get; set; } | Obtient ou définit le nom du style appliqué à la balise de document structuré. |
| [Tag](../../aspose.words.markup/structureddocumenttag/tag/) { get; set; } | Spécifie une balise associée au nœud SDT actuel. Ne peut pas être nul. |
| [Title](../../aspose.words.markup/structureddocumenttag/title/) { get; set; } | Spécifie le nom convivial associé à ce **TDS** . Ne peut pas être nul. |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttag/wordopenxml/) { get; } | Obtient une chaîne qui représente le XML contenu dans le nœud duFlatOpc format. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttag/xmlmapping/) { get; } | Obtient un objet qui représente le mappage de cette balise de document structuré aux données XML dans une partie XML personnalisée du document actuel. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttag/accept/)(DocumentVisitor) | Accepte un visiteur. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Ajoute le nœud spécifié à la fin de la liste des nœuds enfants pour ce nœud. |
| [Clear](../../aspose.words.markup/structureddocumenttag/clear/)() | Efface le contenu de cette balise de document structuré et affiche un espace réservé s'il est défini. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un doublon du nœud. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Réservé à l'utilisation du système. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtient le premier ancêtre du spécifié[`NodeType`](../../aspose.words/nodetype/) . |
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
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtient le nœud précédent selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Supprime le nœud enfant spécifié. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttag/removeselfonly/)() | Supprime uniquement ce nœud SDT lui-même, mais en conserve le contenu dans l'arborescence du document. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Supprime tout[`SmartTag`](../smarttag/) nœuds descendants du nœud actuel. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Sélectionne le premier nœud qui correspond à l'expression XPath. |
| [SetCheckedSymbol](../../aspose.words.markup/structureddocumenttag/setcheckedsymbol/)(int, string) | Définit le symbole utilisé pour représenter l'état coché d'un contrôle de contenu de case à cocher. |
| [SetUncheckedSymbol](../../aspose.words.markup/structureddocumenttag/setuncheckedsymbol/)(int, string) | Définit le symbole utilisé pour représenter l'état non coché d'un contrôle de contenu de case à cocher. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporte le contenu du nœud dans une chaîne à l'aide des options d'enregistrement spécifiées. |

### Remarques

Les balises de document structuré (SDT) permettent d'intégrer la sémantique définie par le client ainsi que son comportement et son apparence dans un document.

Dans cette version, Aspose.Words fournit un certain nombre de méthodes et de propriétés publiques pour manipuler le comportement et le contenu de[`StructuredDocumentTag`](./structureddocumenttag/) . Le mappage des nœuds SDT vers des packages XML personnalisés dans un document peut être effectué en utilisant le[`XmlMapping`](./xmlmapping/) propriété.

[`StructuredDocumentTag`](./structureddocumenttag/) peut apparaître dans un document aux endroits suivants :

* Niveau bloc - Parmi les paragraphes et les tableaux, en tant qu'enfant d'un[`Body`](../../aspose.words/body/) ,[`HeaderFooter`](../../aspose.words/headerfooter/) , [`Comment`](../../aspose.words/comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) ou un[`Shape`](../../aspose.words.drawing/shape/) nœud.
* Niveau ligne - Parmi les lignes d'une table, en tant qu'enfant d'un[`Table`](../../aspose.words.tables/table/) nœud.
* Au niveau de la cellule - Parmi les cellules d'une ligne de tableau, en tant qu'enfant d'un[`Row`](../../aspose.words.tables/row/) nœud.
* Inline-level - Parmi le contenu en ligne à l'intérieur, en tant qu'enfant d'un[`Paragraph`](../../aspose.words/paragraph/).
* Niché dans un autre[`StructuredDocumentTag`](./structureddocumenttag/).

### Exemples

Montre comment utiliser les styles pour les éléments de contrôle de contenu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous deux manières d'appliquer un style du document à une balise de document structuré.
// 1 - Appliquez un objet de style à partir de la collection de styles du document :
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Référencez un style dans le document par son nom :
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### Voir également

* class [CompositeNode](../../aspose.words/compositenode/)
* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* espace de noms [Aspose.Words.Markup](../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
