---
title: VisitBuildingBlockStart
second_title: Aspose.Words für .NET-API-Referenz
description: Wird aufgerufen wenn die Enumeration eines Bausteins gestartet wurde.
type: docs
weight: 70
url: /de/net/aspose.words/documentvisitor/visitbuildingblockstart/
---
## DocumentVisitor.VisitBuildingBlockStart method

Wird aufgerufen, wenn die Enumeration eines Bausteins gestartet wurde.

```csharp
public virtual VisitorAction VisitBuildingBlockStart(BuildingBlock block)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| block | BuildingBlock | Das Objekt, das besucht wird. |

### Rückgabewert

EIN[`VisitorAction`](../../visitoraction/) Wert, der angibt, wie die Enumeration fortgesetzt werden soll.

### Bemerkungen

Hinweis: Ein Bausteinknoten und seine Kinder werden nicht besucht, wenn Sie a Visitor über a ausführen[`Document`](../../document/) Wenn Sie einen Besucher über einen -Baustein ausführen möchten, müssen Sie den Besucher über ausführen[`GlossaryDocument`](../../../aspose.words.buildingblocks/glossarydocument/) or anrufen[`Accept`](../../../aspose.words.buildingblocks/buildingblock/accept/) .

### Beispiele

Zeigt Wege für den Zugriff auf Bausteine in einem Glossardokument.

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
    // 1 - Holen Sie sich die ersten/letzten Bausteine in der Sammlung:
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - Holen Sie sich einen Baustein nach Index:
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 - Holen Sie sich den ersten Baustein, der zu einer Galerie, einem Namen und einer Kategorie passt:
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // Wir werden dies mit einem benutzerdefinierten Besucher tun,
    // was jedem BuildingBlock im GlossaryDocument eine eindeutige GUID gibt
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    glossaryDoc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // In Microsoft Word erreichen wir die Bausteine über "Einfügen" -> "Schnelle Teile" -> "Baustein-Organizer".
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

* enum [VisitorAction](../../visitoraction/)
* class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* class [DocumentVisitor](../)
* namensraum [Aspose.Words](../../documentvisitor/)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
