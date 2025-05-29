---
title: BuildingBlockCollection Class
linktitle: BuildingBlockCollection
articleTitle: BuildingBlockCollection
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words BuildingBlockCollection, un outil puissant pour gérer efficacement les objets BuildingBlock des documents et améliorer votre flux de travail.
type: docs
weight: 340
url: /fr/net/aspose.words.buildingblocks/buildingblockcollection/
---
## BuildingBlockCollection class

Une collection de[`BuildingBlock`](../buildingblock/) objets dans le document.

Pour en savoir plus, visitez le[Modèle d'objet de document (DOM) Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) article de documentation.

```csharp
public class BuildingBlockCollection : NodeCollection
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Obtient le nombre de nœuds dans la collection. |
| [Item](../../aspose.words.buildingblocks/buildingblockcollection/item/) { get; } | Récupère un bloc de construction à l'index donné. (2 indexers) |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../../aspose.words/node/)*) | Ajoute un nœud à la fin de la collection. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Supprime tous les nœuds de cette collection et du document. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../../aspose.words/node/)*) | Détermine si un nœud est dans la collection. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Fournit une itération simple de style « foreach » sur la collection de nœuds. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../../aspose.words/node/)*) | Renvoie l'index de base zéro du nœud spécifié. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../../aspose.words/node/)*) | Insère un nœud dans la collection à l'index spécifié. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../../aspose.words/node/)*) | Supprime le nœud de la collection et du document. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Supprime le nœud à l'index spécifié de la collection et du document. |
| [ToArray](../../aspose.words.buildingblocks/buildingblockcollection/toarray/#toarray)() | Copie tous les blocs de construction de la collection vers un nouveau tableau de blocs de construction. (2 methods) |

## Remarques

Vous ne créez pas d'instances de cette classe directement. Pour accéder à une collection de blocs de construction, utilisez la commande[`BuildingBlocks`](../glossarydocument/buildingblocks/) propriété.

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

* class [NodeCollection](../../aspose.words/nodecollection/)
* espace de noms [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* Assemblée [Aspose.Words](../../)
