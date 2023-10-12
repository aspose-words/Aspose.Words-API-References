---
title: Class GlossaryDocument
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.BuildingBlocks.GlossaryDocument classe. Représente lélément racine dun document glossaire dans un document Word. Un document glossaire est un stockage pour linsertion automatique les entrées de correction automatique et les blocs de construction.
type: docs
weight: 180
url: /fr/net/aspose.words.buildingblocks/glossarydocument/
---
## GlossaryDocument class

Représente l'élément racine d'un document glossaire dans un document Word. Un document glossaire est un stockage pour l'insertion automatique, les entrées de correction automatique et les blocs de construction.

Pour en savoir plus, visitez le[Modèle objet de document (DOM) Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) article documentaire.

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
| [BuildingBlocks](../../aspose.words.buildingblocks/glossarydocument/buildingblocks/) { get; } | Renvoie une collection typée qui représente tous les éléments constitutifs du document glossaire. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtient le nombre d'enfants immédiats de ce nœud. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | Obtient cette instance. |
| [FirstBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/firstbuildingblock/) { get; } | Obtient le premier élément de base du document glossaire. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtient le premier enfant du nœud. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Fournit un accès aux propriétés des polices utilisées dans ce document. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Retours`vrai` si ce nœud a des nœuds enfants. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Retours`vrai` car ce nœud peut avoir des nœuds enfants. |
| [LastBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/lastbuildingblock/) { get; } | Obtient le dernier élément de base du document glossaire. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtient le dernier enfant du nœud. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Donne accès au formatage de liste utilisé dans le document. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Appelé lorsqu'un nœud est inséré ou supprimé dans le document. |
| override [NodeType](../../aspose.words.buildingblocks/glossarydocument/nodetype/) { get; } | Renvoie leGlossaryDocument valeur. |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Obtient ou définit la couleur de la page du document. Cette propriété est une version plus simple de[`BackgroundShape`](../../aspose.words/documentbase/backgroundshape/) . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un[`Range`](../../aspose.words/range/) objet qui représente la partie d'un document contenue dans ce nœud. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Permet de contrôler la manière dont les ressources externes sont chargées. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Renvoie une collection de styles définis dans le document. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Appelé lors de diverses procédures de traitement de documents lorsqu'un problème est détecté qui pourrait entraîner une perte de fidélité des données ou du formatage. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/glossarydocument/accept/)(DocumentVisitor) | Accepte un visiteur. |
| override [AcceptEnd](../../aspose.words.buildingblocks/glossarydocument/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words.buildingblocks/glossarydocument/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un duplicata du nœud. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crée un navigateur qui peut être utilisé pour parcourir et lire des nœuds. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtient le premier ancêtre du spécifié[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtient le premier ancêtre du type d'objet spécifié. |
| [GetBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/getbuildingblock/)(BuildingBlockGallery, string, string) | Recherche un bloc de construction en utilisant la galerie, la catégorie et le nom spécifiés. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Renvoie un Nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Renvoie une collection active de nœuds enfants qui correspondent au type spécifié. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fournit la prise en charge de chaque itération de style sur les nœuds enfants de ce nœud. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Récupère le texte de ce nœud et de tous ses enfants. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(Node, bool) | Importe un nœud d'un autre document vers le document actuel. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(Node, bool, ImportFormatMode) | Importe un nœud d'un autre document vers le document actuel avec une option pour contrôler le formatage. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Renvoie l'index du nœud enfant spécifié dans le tableau de nœuds enfants. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtient le nœud suivant selon l'algorithme de traversée de l'arbre de pré-commande. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtient le nœud précédent selon l'algorithme de traversée d'arbre de pré-commande. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Supprime tout[`SmartTag`](../../aspose.words.markup/smarttag/)nœuds descendants du nœud actuel. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Sélectionne le premier[`Node`](../../aspose.words/node/) qui correspond à l'expression XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporte le contenu du nœud dans une chaîne à l'aide des options de sauvegarde spécifiées. |

### Remarques

Certains documents, généralement des modèles, peuvent contenir de l'insertion automatique, des entrées de correction automatique et/ou des blocs de construction (également appelésentrées de document de glossaire ,parties de documents oublocs de construction).

Pour accéder aux blocs de construction, vous devez charger un document dans un[`Document`](../../aspose.words/document/) Objet . Les blocs de construction seront disponibles via le[`GlossaryDocument`](../../aspose.words/document/glossarydocument/) propriété.

`GlossaryDocument` peut contenir n'importe quel nombre de[`BuildingBlock`](../buildingblock/) objets. Chacun[`BuildingBlock`](../buildingblock/) représente une partie du document.

Correspond au **glossaireDocument** et **docParts** éléments en OOXML.

### Exemples

Montre les moyens d'accéder aux blocs de construction dans un document glossaire.

```csharp
public void GlossaryDocument()
{
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();

    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 1" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 2" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 3" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 4" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 5" });

    Assert.AreEqual(5, glossaryDoc.BuildingBlocks.Count);

    doc.GlossaryDocument = glossaryDoc;

    // Il existe différentes manières d'accéder aux blocs de construction.
    // 1 - Récupère les premier/dernier blocs de construction de la collection :
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - Récupère un bloc de construction par index :
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 - Obtenez le premier bloc de construction qui correspond à une galerie, un nom et une catégorie :
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // Nous ferons cela en utilisant un visiteur personnalisé,
    // qui donnera à chaque BuildingBlock du GlossaryDocument un GUID unique
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    glossaryDoc.Accept(visitor);
    Console.WriteLine(visitor.GetText());

    // Dans Microsoft Word, nous pouvons accéder aux blocs de construction via "Insérer" -> "Pièces rapides" -> "Organisateur de blocs de construction".
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// Donne à chaque bloc de construction d'un document de glossaire visité un GUID unique.
/// Stocke les paires de blocs de construction GUID dans un dictionnaire.
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


