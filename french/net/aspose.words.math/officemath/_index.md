---
title: OfficeMath
second_title: Référence de l'API Aspose.Words pour .NET
description: Représente un objet Office Math tel quune fonction une équation une matrice ou similaire. Peut contenir des éléments enfants  y compris des séries de texte mathématique des signets des commentaires dautresOfficeMath./officemath instances et quelques autres nœuds.
type: docs
weight: 3880
url: /fr/net/aspose.words.math/officemath/
---
## OfficeMath class

Représente un objet Office Math tel qu'une fonction, une équation, une matrice ou similaire. Peut contenir des éléments enfants , y compris des séries de texte mathématique, des signets, des commentaires, d'autres[`OfficeMath`](../officemath) instances et quelques autres nœuds.

```csharp
public class OfficeMath : CompositeNode
```

## Propriétés

| Nom | La description |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Obtient tous les nœuds enfants immédiats de ce nœud. |
| [Count](../../aspose.words/compositenode/count) { get; } | Obtient le nombre d'enfants immédiats de ce nœud. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| [DisplayType](../../aspose.words.math/officemath/displaytype) { get; set; } | Obtient/définit le type de format d'affichage Office Math qui indique si une équation est affichée en ligne avec le texte ou affichée sur sa propre ligne. |
| virtual [Document](../../aspose.words/node/document) { get; } | Obtient le document auquel ce nœud appartient. |
| [EquationXmlEncoding](../../aspose.words.math/officemath/equationxmlencoding) { get; set; } | Obtient/définit un encodage qui a été utilisé pour encoder l'équation XML, si cet objet mathématique de bureau est lu à partir de equation XML. Nous utilisons l'encodage lors de l'enregistrement d'un document pour écrire dans le même encodage qu'il a été lu. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Obtient le premier enfant du nœud. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Renvoie vrai si ce nœud a des nœuds enfants. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Renvoie true car ce nœud peut avoir des nœuds enfants. |
| [Justification](../../aspose.words.math/officemath/justification) { get; set; } | Obtient/définit la justification Office Math. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Obtient le dernier enfant du nœud. |
| [MathObjectType](../../aspose.words.math/officemath/mathobjecttype) { get; } | Obtient le type[`MathObjectType`](./mathobjecttype) de cet objet Office Math. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words.math/officemath/nodetype) { get; } | Retours **NodeType.OfficeMathNodeType.OfficeMath** . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Obtient le parent immédiat de ce nœud. |
| [ParentParagraph](../../aspose.words.math/officemath/parentparagraph) { get; } | Récupère le parent[`Paragraph`](../../aspose.words/paragraph) de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range) { get; } | Renvoie un **Intervalle** objet qui représente la partie d'un document contenue dans ce nœud. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words.math/officemath/accept)(DocumentVisitor) | Accepte un visiteur. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Ajoute le nœud spécifié à la fin de la liste des nœuds enfants pour ce nœud. |
| [Clone](../../aspose.words/node/clone)(bool) | Crée un doublon du nœud. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Réservé à l'utilisation du système. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Obtient le premier ancêtre du spécifié[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Obtient le premier ancêtre du type d'objet spécifié. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Renvoie un Nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Renvoie une collection dynamique de nœuds enfants correspondant au type spécifié. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Fournit la prise en charge de chaque itération de style sur les nœuds enfants de ce nœud. |
| [GetMathRenderer](../../aspose.words.math/officemath/getmathrenderer)() | Crée et renvoie un objet qui peut être utilisé pour rendre cette équation dans une image. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Obtient le texte de ce nœud et de tous ses enfants. |
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

Dans cette version d'Aspose.Words,[`OfficeMath`](../officemath) Les nœuds ne fournissent pas de méthodes publiques et de propriétés pour créer ou modifier un objet OfficeMath. Dans cette version, vous ne pouvez pas instancier Math nœuds ou modifier les nœuds existants, sauf en les supprimant.

[`OfficeMath`](../officemath) ne peut être qu'un enfant de[`Paragraph`](../../aspose.words/paragraph).

### Exemples

Montre comment définir la mise en forme de l'affichage mathématique de bureau.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// Les nœuds OfficeMath qui sont des enfants d'autres nœuds OfficeMath sont toujours en ligne.
// Le nœud avec lequel nous travaillons est le nœud de base pour changer son emplacement et son type d'affichage.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// Les formats OOXML et WML utilisent la propriété "EquationXmlEncoding".
Assert.IsNull(officeMath.EquationXmlEncoding);

// Modifier l'emplacement et le type d'affichage du nœud OfficeMath.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Voir également

* class [CompositeNode](../../aspose.words/compositenode)
* espace de noms [Aspose.Words.Math](../../aspose.words.math)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
