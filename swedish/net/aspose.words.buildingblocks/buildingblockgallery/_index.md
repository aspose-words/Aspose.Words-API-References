---
title: BuildingBlockGallery Enum
linktitle: BuildingBlockGallery
articleTitle: BuildingBlockGallery
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words BuildingBlockGallery enum, din guide till fördefinierade gallerier för effektiv dokumenthantering och organisation. Förbättra ditt arbetsflöde idag!
type: docs
weight: 350
url: /sv/net/aspose.words.buildingblocks/buildingblockgallery/
---
## BuildingBlockGallery enumeration

Anger det fördefinierade galleriet som ett byggblock klassificeras i.

```csharp
public enum BuildingBlockGallery
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| All | `0` | Anger att denna ordlistadokumentpost ska associeras med alla möjliga galleriklassificeringsvärden. |
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
| Default | `0` | Samma somAll . |

## Anmärkningar

Motsvarar den**ST_DocPartGallery** skriv in OOXML.

## Exempel

Visar sätt att komma åt byggstenar i ett ordlistadokument.

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

    // Det finns olika sätt att komma åt byggstenar.
    // 1 - Hämta de första/sista byggstenarna i samlingen:
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - Hämta en byggsten via index:
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 - Hämta den första byggstenen som matchar ett galleri, namn och kategori:
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // Vi gör det med hjälp av en anpassad besökare,
    // vilket ger varje BuildingBlock i GlossaryDocument ett unikt GUID
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    // Besök början/slutet av ordlistadokumentet.
    glossaryDoc.Accept(visitor);
    // Besök endast början av ordlistadokumentet.
    glossaryDoc.AcceptStart(visitor);
    // Besök endast slutet av ordlistadokumentet.
    glossaryDoc.AcceptEnd(visitor);
    Console.WriteLine(visitor.GetText());

    // I Microsoft Word kan vi komma åt byggstenarna via "Insert" -> "Quick Parts" -> "Building Blocks Organizer".
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// Ger varje byggsten i ett besökt ordlistadokument ett unikt GUID.
/// Lagrar GUID-byggstensparen i en ordbok.
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

* namnutrymme [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* hopsättning [Aspose.Words](../../)
