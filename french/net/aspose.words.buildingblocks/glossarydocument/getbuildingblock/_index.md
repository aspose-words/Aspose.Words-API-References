---
title: GetBuildingBlock
second_title: Référence de l'API Aspose.Words pour .NET
description: Trouve un bloc de construction en utilisant la galerie la catégorie et le nom spécifiés.
type: docs
weight: 70
url: /fr/net/aspose.words.buildingblocks/glossarydocument/getbuildingblock/
---
## GlossaryDocument.GetBuildingBlock method

Trouve un bloc de construction en utilisant la galerie, la catégorie et le nom spécifiés.

```csharp
public BuildingBlock GetBuildingBlock(BuildingBlockGallery gallery, string category, string name)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| gallery | BuildingBlockGallery | Les critères de la galerie. |
| category | String | Les critères de la catégorie. Peut être nul, auquel cas il ne sera pas utilisé pour la comparaison. |
| name | String | Les critères de nom de bloc de construction. |

### Return_Value

Le bloc de construction correspondant ou null si aucune correspondance n'a été trouvée.

### Remarques

Il s'agit d'une méthode pratique qui itère sur tous les blocs de construction de cette collection et renvoie le premier bloc de construction qui correspond à la galerie, à la catégorie et au nom spécifiés.

Microsoft Word organise les blocs de construction en galeries. Les galleries sont prédéfinies à l'aide de la[`BuildingBlockGallery`](../../buildingblockgallery) enum. Dans chaque galerie, les blocs de construction peuvent être organisés en une ou plusieurs catégories. Le nom de la catégorie est une chaîne. Chaque bloc de construction porte un nom. Il n'est pas garanti qu'un nom de bloc de construction soit unique.

### Exemples

Montre les moyens d'accéder aux blocs de construction dans un document de glossaire.

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
    // 1 - Récupère les premiers/derniers blocs de construction de la collection :
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - Récupère un bloc de construction par index :
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 - Récupérez le premier bloc de construction qui correspond à une galerie, un nom et une catégorie :
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // Nous le ferons en utilisant un visiteur personnalisé,
    // qui donnera à chaque BuildingBlock dans le GlossaryDocument un GUID unique
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    glossaryDoc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // Dans Microsoft Word, nous pouvons accéder aux blocs de construction via "Insérer" -> "Parties rapides" -> "Organisateur de blocs de construction".
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

* class [BuildingBlock](../../buildingblock)
* enum [BuildingBlockGallery](../../buildingblockgallery)
* class [GlossaryDocument](../../glossarydocument)
* espace de noms [Aspose.Words.BuildingBlocks](../../glossarydocument)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->