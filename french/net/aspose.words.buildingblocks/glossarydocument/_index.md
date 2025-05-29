---
title: GlossaryDocument Class
linktitle: GlossaryDocument
articleTitle: GlossaryDocument
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.BuildingBlocks.GlossaryDocument, votre clé pour gérer de manière transparente le texte automatique et les blocs de construction dans les documents Word.
type: docs
weight: 370
url: /fr/net/aspose.words.buildingblocks/glossarydocument/
---
## GlossaryDocument class

Représente l'élément racine d'un document de glossaire dans un document Word. Un document de glossaire est un espace de stockage pour les entrées de texte automatique, de correction automatique et les blocs de construction.

Pour en savoir plus, visitez le[Modèle d'objet de document (DOM) Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) article de documentation.

```csharp
public class GlossaryDocument : DocumentBase
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [GlossaryDocument](glossarydocument/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Obtient ou définit la forme d'arrière-plan du document. Peut être`nul` . |
| [BuildingBlocks](../../aspose.words.buildingblocks/glossarydocument/buildingblocks/) { get; } | Renvoie une collection typée qui représente tous les blocs de construction du document de glossaire. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtient le nombre d'enfants immédiats de ce nœud. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | Obtient cette instance. |
| [FirstBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/firstbuildingblock/) { get; } | Obtient le premier bloc de construction dans le document de glossaire. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtient le premier enfant du nœud. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Donne accès aux propriétés des polices utilisées dans ce document. |
| [FootnoteSeparators](../../aspose.words/documentbase/footnoteseparators/) { get; } | Donne accès aux séparateurs de notes de bas de page/de fin définis dans le document. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Retours`vrai` si ce nœud a des nœuds enfants. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Retours`vrai` car ce nœud peut avoir des nœuds enfants. |
| [LastBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/lastbuildingblock/) { get; } | Obtient le dernier bloc de construction dans le document de glossaire. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtient le dernier enfant du nœud. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Donne accès au formatage de liste utilisé dans le document. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Appelé lorsqu'un nœud est inséré ou supprimé dans le document. |
| override [NodeType](../../aspose.words.buildingblocks/glossarydocument/nodetype/) { get; } | Renvoie leGlossaryDocument valeur. |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Obtient ou définit la couleur de page du document. Cette propriété est une version simplifiée de[`BackgroundShape`](../../aspose.words/documentbase/backgroundshape/) . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un[`Range`](../../aspose.words/range/)objet qui représente la partie d'un document contenue dans ce nœud. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Permet de contrôler la manière dont les ressources externes sont chargées. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Renvoie une collection de styles définis dans le document. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Appelé lors de diverses procédures de traitement de documents lorsqu'un problème est détecté qui pourrait entraîner une perte de fidélité des données ou du formatage. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/glossarydocument/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepte un visiteur. |
| override [AcceptEnd](../../aspose.words.buildingblocks/glossarydocument/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepte un visiteur pour visiter la fin du document Glossaire. |
| override [AcceptStart](../../aspose.words.buildingblocks/glossarydocument/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepte un visiteur pour visiter le début du document Glossaire. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Ajoute le nœud spécifié à la fin de la liste des nœuds enfants pour ce nœud. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crée un doublon du nœud. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crée un navigateur qui peut être utilisé pour parcourir et lire les nœuds. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Obtient le premier ancêtre du spécifié[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtient le premier ancêtre du type d'objet spécifié. |
| [GetBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/getbuildingblock/)(*[BuildingBlockGallery](../buildingblockgallery/), string, string*) | Recherche un bloc de construction en utilisant la galerie, la catégorie et le nom spécifiés. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Renvoie un Nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Renvoie une collection active de nœuds enfants qui correspondent au type spécifié. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fournit un support pour chaque itération de style sur les nœuds enfants de ce nœud. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Obtient le texte de ce nœud et de tous ses enfants. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../../aspose.words/node/), bool*) | Importe un nœud d'un autre document vers le document actuel. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../../aspose.words/node/), bool, [ImportFormatMode](../../aspose.words/importformatmode/)*) | Importe un nœud d'un autre document vers le document actuel avec une option pour contrôler le formatage. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Renvoie l'index du nœud enfant spécifié dans le tableau de nœuds enfants. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Insère le nœud spécifié immédiatement après le nœud de référence spécifié. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Insère le nœud spécifié immédiatement avant le nœud de référence spécifié. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Obtient le nœud suivant selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Ajoute le nœud spécifié au début de la liste des nœuds enfants pour ce nœud. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Obtient le nœud précédent selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Supprime le nœud enfant spécifié. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Supprime tout[`SmartTag`](../../aspose.words.markup/smarttag/) nœuds descendants du nœud actuel. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Sélectionne le premier[`Node`](../../aspose.words/node/) qui correspond à l'expression XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporte le contenu du nœud dans une chaîne en utilisant les options de sauvegarde spécifiées. |

## Remarques

Certains documents, généralement des modèles, peuvent contenir du texte automatique, des entrées de correction automatique et/ou des blocs de construction (également appelésentrées de document du glossaire ,parties du document oublocs de construction).

Pour accéder aux blocs de construction, vous devez charger un document dans un[`Document`](../../aspose.words/document/) Objet . Les blocs de construction seront disponibles via[`GlossaryDocument`](../../aspose.words/document/glossarydocument/) propriété.

`GlossaryDocument` peut contenir n'importe quel nombre de[`BuildingBlock`](../buildingblock/)objets. Chaque[`BuildingBlock`](../buildingblock/) représente une partie du document.

Correspond à la**glossaireDocument** et**docParts**éléments dans OOXML.

## Exemples

Montre les moyens d’accéder aux blocs de construction dans un document de glossaire.

```csharp
public void GlossaryDocument()
{
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();

    BuildingBlock child1 = new BuildingBlock(glossaryDoc) { Name = "Block 1" };
    glossaryDoc.AppendChild(child1);
    BuildingBlock child2 = new BuildingBlock(glossaryDoc) { Name = "Block 2" };
    glossaryDoc.AppendChild(child2);
    BuildingBlock child3 = new BuildingBlock(glossaryDoc) { Name = "Block 3" };
    glossaryDoc.AppendChild(child3);
    BuildingBlock child4 = new BuildingBlock(glossaryDoc) { Name = "Block 4" };
    glossaryDoc.AppendChild(child4);
    BuildingBlock child5 = new BuildingBlock(glossaryDoc) { Name = "Block 5" };
    glossaryDoc.AppendChild(child5);

    Assert.AreEqual(5, glossaryDoc.BuildingBlocks.Count);

    doc.GlossaryDocument = glossaryDoc;

    // Il existe différentes manières d’accéder aux blocs de construction.
    // 1 - Obtenir les premier/dernier blocs de construction de la collection :
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - Obtenir un bloc de construction par index :
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 - Obtenir le premier bloc de construction qui correspond à une galerie, un nom et une catégorie :
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // Nous le ferons en utilisant un visiteur personnalisé,
    // qui donnera à chaque BuildingBlock du GlossaryDocument un GUID unique
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    // Visitez le début/la fin du document Glossaire.
    glossaryDoc.Accept(visitor);
    // Visitez uniquement le début du document Glossaire.
    glossaryDoc.AcceptStart(visitor);
    // Visitez uniquement la fin du document Glossaire.
    glossaryDoc.AcceptEnd(visitor);
    Console.WriteLine(visitor.GetText());

    // Dans Microsoft Word, nous pouvons accéder aux blocs de construction via « Insertion » -> « Parties rapides » -> « Organisateur de blocs de construction ».
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// Attribue à chaque bloc de construction d'un document de glossaire visité un GUID unique.
/// Stocke les paires GUID-bloc de construction dans un dictionnaire.
/// </summary>
public class GlossaryDocVisitor : DocumentVisitor
{
    public GlossaryDocVisitor()
    {
        mBlocksByGuid = new Dictionary<Guid, BuildingBlock>();
        mBuilder = new StringBuilder();
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    public Dictionary<Guid, BuildingBlock> GetDictionary()
    {
        return mBlocksByGuid;
    }

    public override VisitorAction VisitGlossaryDocumentStart(GlossaryDocument glossary)
    {
        mBuilder.AppendLine("Glossary document found!");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitGlossaryDocumentEnd(GlossaryDocument glossary)
    {
        mBuilder.AppendLine("Reached end of glossary!");
        mBuilder.AppendLine("BuildingBlocks found: " + mBlocksByGuid.Count);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockStart(BuildingBlock block)
    {
        block.Guid = Guid.NewGuid();
        mBlocksByGuid.Add(block.Guid, block);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockEnd(BuildingBlock block)
    {
        mBuilder.AppendLine("\tVisited block \"" + block.Name + "\"");
        mBuilder.AppendLine("\t Type: " + block.Type);
        mBuilder.AppendLine("\t Gallery: " + block.Gallery);
        mBuilder.AppendLine("\t Behavior: " + block.Behavior);
        mBuilder.AppendLine("\t Description: " + block.Description);

        return VisitorAction.Continue;
    }

    private readonly Dictionary<Guid, BuildingBlock> mBlocksByGuid;
    private readonly StringBuilder mBuilder;
}
```

### Voir également

* class [DocumentBase](../../aspose.words/documentbase/)
* espace de noms [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* Assemblée [Aspose.Words](../../)
