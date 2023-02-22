---
title: Class BuildingBlockCollection
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.BuildingBlocks.BuildingBlockCollection klass. En samling avBuildingBlock objekt i dokumentet.
type: docs
weight: 140
url: /sv/net/aspose.words.buildingblocks/buildingblockcollection/
---
## BuildingBlockCollection class

En samling av[`BuildingBlock`](../buildingblock/) objekt i dokumentet.

```csharp
public class BuildingBlockCollection : NodeCollection
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Hämtar antalet noder i samlingen. |
| [Item](../../aspose.words.buildingblocks/buildingblockcollection/item/) { get; } | Hämtar ett byggblock vid det givna indexet. (2 indexers) |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | Lägger till en nod i slutet av samlingen. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Tar bort alla noder från den här samlingen och från dokumentet. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | Bestämmer om en nod finns i samlingen. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Ger en enkel "foreach" stil iteration över samlingen av noder. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | Returnerar det nollbaserade indexet för den angivna noden. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | Infogar en nod i samlingen vid det angivna indexet. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | Tar bort noden från samlingen och från dokumentet. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | Tar bort noden vid det angivna indexet från samlingen och från dokumentet. |
| [ToArray](../../aspose.words.buildingblocks/buildingblockcollection/toarray/#toarray)() | Kopierar alla byggstenar från samlingen till en ny uppsättning byggstenar. (2 methods) |

### Anmärkningar

Du skapar inte instanser av den här klassen direkt. För att komma åt en samling av byggstenar använd[`BuildingBlocks`](../glossarydocument/buildingblocks/) fast egendom.

### Exempel

Visar sätt att komma åt byggstenar i ett ordlistadokument.

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

    // Det finns olika sätt att komma åt byggstenar.
    // 1 - Få de första/sista byggstenarna i samlingen:
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - Få en byggsten efter index:
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 - Få den första byggstenen som matchar ett galleri, namn och kategori:
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // Vi kommer att göra det med en anpassad besökare,
    // som kommer att ge varje byggnadsblock i ordlistadokumentet en unik GUID
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    glossaryDoc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // I Microsoft Word kan vi komma åt byggstenarna via "Infoga" -> "Snabbdelar" -> "Byggstensarrangör".
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// Ger varje byggsten i ett besökt ordlistadokument en unik GUID.
/// Lagrar GUID-byggblocksparen i en ordbok.
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

### Se även

* class [NodeCollection](../../aspose.words/nodecollection/)
* namnutrymme [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* hopsättning [Aspose.Words](../../)


