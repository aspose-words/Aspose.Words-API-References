---
title: DocumentBase
second_title: Référence de l'API Aspose.Words pour .NET
description: Fournit la classe de base abstraite pour un document principal et un document glossaire dun document Word.
type: docs
weight: 430
url: /fr/net/aspose.words/documentbase/
---
## DocumentBase class

Fournit la classe de base abstraite pour un document principal et un document glossaire d'un document Word.

```csharp
public abstract class DocumentBase : CompositeNode
```

## Propriétés

| Nom | La description |
| --- | --- |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape) { get; set; } | Obtient ou définit la forme d'arrière-plan du document. Peut être null. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Obtient tous les nœuds enfants immédiats de ce nœud. |
| [Count](../../aspose.words/compositenode/count) { get; } | Obtient le nombre d'enfants immédiats de ce nœud. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| override [Document](../../aspose.words/documentbase/document) { get; } |  |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Obtient le premier enfant du nœud. |
| [FontInfos](../../aspose.words/documentbase/fontinfos) { get; } | Fournit un accès aux propriétés des polices utilisées dans ce document. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Renvoie vrai si ce nœud a des nœuds enfants. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Renvoie true car ce nœud peut avoir des nœuds enfants. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Obtient le dernier enfant du nœud. |
| [Lists](../../aspose.words/documentbase/lists) { get; } | Fournit l'accès à la mise en forme de liste utilisée dans le document. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback) { get; set; } | Appelé lorsqu'un nœud est inséré ou supprimé dans le document. |
| abstract [NodeType](../../aspose.words/node/nodetype) { get; } | Obtient le type de ce nœud. |
| [PageColor](../../aspose.words/documentbase/pagecolor) { get; set; } | Obtient ou définit la couleur de page du document. Cette propriété est une version simplifiée de[`BackgroundShape`](./backgroundshape) . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Obtient le parent immédiat de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range) { get; } | Renvoie un **Intervalle** objet qui représente la partie d'un document contenue dans ce nœud. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback) { get; set; } | Permet de contrôler le chargement des ressources externes. |
| [Styles](../../aspose.words/documentbase/styles) { get; } | Renvoie une collection de styles définis dans le document. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback) { get; set; } | Appelé lors de diverses procédures de traitement de documents lorsqu'un problème est détecté pouvant entraîner une perte de fidélité des données ou du formatage. |

## Méthodes

| Nom | La description |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept)(DocumentVisitor) | Accepte un visiteur. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Ajoute le nœud spécifié à la fin de la liste des nœuds enfants pour ce nœud. |
| [Clone](../../aspose.words/node/clone)(bool) | Crée un doublon du nœud. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Réservé à l'utilisation du système. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Obtient le premier ancêtre du spécifié[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Obtient le premier ancêtre du type d'objet spécifié. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Renvoie un Nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Renvoie une collection dynamique de nœuds enfants correspondant au type spécifié. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Fournit la prise en charge de chaque itération de style sur les nœuds enfants de ce nœud. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Obtient le texte de ce nœud et de tous ses enfants. |
| [ImportNode](../../aspose.words/documentbase/importnode#importnode)(Node, bool) | Importe un nœud d'un autre document vers le document actuel. |
| [ImportNode](../../aspose.words/documentbase/importnode#importnode_1)(Node, bool, ImportFormatMode) | Importe un nœud d'un autre document vers le document actuel avec une option pour contrôler la mise en forme. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Renvoie l'index du nœud enfant spécifié dans le tableau de nœuds enfants. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Insère le nœud spécifié immédiatement après le nœud de référence spécifié. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Insère le nœud spécifié juste avant le nœud de référence spécifié. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Obtient le nœud suivant selon l'algorithme de traversée de l'arbre de pré-ordre. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Ajoute le nœud spécifié au début de la liste des nœuds enfants pour ce nœud. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Obtient le nœud précédent selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [Remove](../../aspose.words/node/remove)() | Se supprime du parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Supprime le nœud enfant spécifié. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Supprime tout[`SmartTag`](../../aspose.words.markup/smarttag) nœuds descendants du nœud actuel. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Sélectionne le premier nœud qui correspond à l'expression XPath. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exporte le contenu du nœud dans une chaîne à l'aide des options d'enregistrement spécifiées. |

### Remarques

Aspose.Words représente un document Word sous la forme d'une arborescence de nœuds.[`DocumentBase`](../documentbase) est un nœud racine de l'arborescence qui contient tous les autres nœuds du document.

[`DocumentBase`](../documentbase) stocke également des informations à l'échelle du document telles que[`Styles`](./styles) et [`Lists`](./lists) auxquels les nœuds de l'arbre peuvent se référer.

### Exemples

Montre comment initialiser les sous-classes de DocumentBase.

```csharp
Document doc = new Document();

Assert.AreEqual(typeof(DocumentBase), doc.GetType().BaseType);

GlossaryDocument glossaryDoc = new GlossaryDocument();
doc.GlossaryDocument = glossaryDoc;

Assert.AreEqual(typeof(DocumentBase), glossaryDoc.GetType().BaseType);
```

### Voir également

* class [CompositeNode](../compositenode)
* espace de noms [Aspose.Words](../../aspose.words)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
