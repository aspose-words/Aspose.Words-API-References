---
title: GlossaryDocument.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words pour .NET
description: Découvrez la méthode GlossaryDocument Accept qui améliore l'expérience utilisateur en gérant efficacement les interactions des visiteurs. En savoir plus !
type: docs
weight: 60
url: /fr/net/aspose.words.buildingblocks/glossarydocument/accept/
---
## GlossaryDocument.Accept method

Accepte un visiteur.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| visitor | DocumentVisitor | Le visiteur qui visitera les nœuds. |

### Return_Value

Vrai si tous les nœuds ont été visités ; faux si[`DocumentVisitor`](../../../aspose.words/documentvisitor/) a arrêté l'opération avant de visiter tous les nœuds.

## Remarques

Énumère ce nœud et tous ses enfants. Chaque nœud appelle une méthode correspondante sur[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

Pour plus d'informations, consultez le modèle de conception Visitor.

Appels[`VisitGlossaryDocumentStart`](../../../aspose.words/documentvisitor/visitglossarydocumentstart/) , puis appelle[`Accept`](../../../aspose.words/node/accept/) pour tous les nœuds enfants de ce nœud, puis appelle[`VisitGlossaryDocumentEnd`](../../../aspose.words/documentvisitor/visitglossarydocumentend/) à la fin.

Remarque : un nœud de document de glossaire et ses enfants ne sont pas visités lorsque vous exécutez un visiteur sur un[`Document`](../../../aspose.words/document/) . Si vous souhaitez exécuter un visiteur sur un document de glossaire a , vous devez appeler`Accept` .

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

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [GlossaryDocument](../)
* espace de noms [Aspose.Words.BuildingBlocks](../../../aspose.words.buildingblocks/)
* Assemblée [Aspose.Words](../../../)
