---
title: BuildingBlockGallery Enum
linktitle: BuildingBlockGallery
articleTitle: BuildingBlockGallery
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words BuildingBlockGallery, votre guide des galeries prédéfinies pour une gestion et une organisation efficaces de vos documents. Améliorez votre flux de travail dès aujourd'hui !
type: docs
weight: 350
url: /fr/net/aspose.words.buildingblocks/buildingblockgallery/
---
## BuildingBlockGallery enumeration

Spécifie la galerie prédéfinie dans laquelle un bloc de construction est classé.

```csharp
public enum BuildingBlockGallery
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| All | `0` | Spécifie que cette entrée de document de glossaire doit être associée à toutes les valeurs de classification de galerie possibles. |
| AutoText | `1` |  |
| Bibliography | `2` |  |
| CoverPage | `3` |  |
| CustomAutoText | `4` |  |
| CustomBibliography | `5` |  |
| CustomCoverPage | `6` |  |
| CustomEquations | `7` |  |
| CustomFooters | `8` |  |
| CustomHeaders | `9` |  |
| Custom1 | `10` |  |
| Custom2 | `11` |  |
| Custom3 | `12` |  |
| Custom4 | `13` |  |
| Custom5 | `14` |  |
| CustomPageNumber | `15` |  |
| CustomPageNumberAtBottom | `16` |  |
| CustomPageNumberAtMargin | `17` |  |
| CustomPageNumberAtTop | `18` |  |
| CustomQuickParts | `19` |  |
| CustomTableOfContents | `20` |  |
| CustomTables | `21` |  |
| CustomTextBox | `22` |  |
| CustomWatermarks | `23` |  |
| NoGallery | `24` |  |
| QuickParts | `25` |  |
| Equations | `26` |  |
| Footers | `27` |  |
| Headers | `28` |  |
| PageNumber | `29` |  |
| PageNumberAtBottom | `30` |  |
| PageNumberAtMargin | `31` |  |
| PageNumberAtTop | `32` |  |
| StructuredDocumentTagPlaceholderText | `33` |  |
| TableOfContents | `34` |  |
| Tables | `35` |  |
| TextBox | `36` |  |
| Watermarks | `37` |  |
| Default | `0` | Identique àAll . |

## Remarques

Correspond à la**ST_DocPartGallery** tapez OOXML.

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

* espace de noms [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* Assemblée [Aspose.Words](../../)
