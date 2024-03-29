---
title: GlossaryDocument.GetBuildingBlock
linktitle: GetBuildingBlock
articleTitle: GetBuildingBlock
second_title: Aspose.Words für .NET
description: GlossaryDocument GetBuildingBlock methode. Findet einen Baustein anhand der angegebenen Galerie Kategorie und des angegebenen Namens in C#.
type: docs
weight: 70
url: /de/net/aspose.words.buildingblocks/glossarydocument/getbuildingblock/
---
## GlossaryDocument.GetBuildingBlock method

Findet einen Baustein anhand der angegebenen Galerie, Kategorie und des angegebenen Namens.

```csharp
public BuildingBlock GetBuildingBlock(BuildingBlockGallery gallery, string category, string name)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| gallery | BuildingBlockGallery | Die Galeriekriterien. |
| category | String | Die Kategoriekriterien. Kann sein`Null`In diesem Fall wird es nicht zum Vergleich herangezogen. |
| name | String | Die Kriterien für den Bausteinnamen. |

### Rückgabewert

Der passende Baustein bzw`Null` wenn keine Übereinstimmung gefunden wurde.

## Bemerkungen

Dies ist eine praktische Methode, die alle Bausteine in dieser Sammlung durchläuft und den ersten Baustein zurückgibt, der mit der angegebenen Galerie, Kategorie und dem angegebenen Namen übereinstimmt.

Microsoft Word organisiert Bausteine in Galerien. Die Galerien sind mit vordefiniert[`BuildingBlockGallery`](../../buildingblockgallery/) enum. Innerhalb jeder Galerie können Bausteine in einer oder mehreren Kategorien organisiert werden. Der Kategoriename ist eine Zeichenfolge. Jeder Baustein hat einen Namen. Es kann nicht garantiert werden, dass der Name eines Bausteins eindeutig ist.

## Beispiele

Zeigt Möglichkeiten für den Zugriff auf Bausteine in einem Glossardokument.

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

    // Es gibt verschiedene Möglichkeiten, auf Bausteine zuzugreifen.
    // 1 – Holen Sie sich die ersten/letzten Bausteine in der Sammlung:
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 – Einen Baustein nach Index abrufen:
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 – Holen Sie sich den ersten Baustein, der einer Galerie, einem Namen und einer Kategorie entspricht:
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // Wir werden das mit einem benutzerdefinierten Besucher tun,
    // wodurch jedem BuildingBlock im GlossaryDocument eine eindeutige GUID zugewiesen wird
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    glossaryDoc.Accept(visitor);
    Console.WriteLine(visitor.GetText());

    // In Microsoft Word können wir über „Einfügen“ -> auf die Bausteine zugreifen. „Schnellteile“ -> „Baustein-Organizer“.
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// Gibt jedem Baustein in einem besuchten Glossardokument eine eindeutige GUID.
/// Speichert die GUID-Bausteinpaare in einem Wörterbuch.
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

### Siehe auch

* class [BuildingBlock](../../buildingblock/)
* enum [BuildingBlockGallery](../../buildingblockgallery/)
* class [GlossaryDocument](../)
* namensraum [Aspose.Words.BuildingBlocks](../../../aspose.words.buildingblocks/)
* Montage [Aspose.Words](../../../)
