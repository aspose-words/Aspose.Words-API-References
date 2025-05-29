---
title: DocumentVisitor.VisitGlossaryDocumentEnd
linktitle: VisitGlossaryDocumentEnd
articleTitle: VisitGlossaryDocumentEnd
second_title: Aspose.Words für .NET
description: Entdecken Sie die Methode VisitGlossaryDocumentEnd in DocumentVisitor. Erfahren Sie, wie sie die Glossardokumentenaufzählung für ein effizientes Datenmanagement verbessert.
type: docs
weight: 240
url: /de/net/aspose.words/documentvisitor/visitglossarydocumentend/
---
## DocumentVisitor.VisitGlossaryDocumentEnd method

Wird aufgerufen, wenn die Aufzählung eines Glossardokuments beendet ist.

```csharp
public virtual VisitorAction VisitGlossaryDocumentEnd(GlossaryDocument glossary)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| glossary | GlossaryDocument | Das Objekt, das besucht wird. |

### Rückgabewert

A[`VisitorAction`](../../visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll.

## Bemerkungen

Hinweis: Ein Glossardokumentknoten und seine untergeordneten Knoten werden nicht besucht, wenn Sie einen Besucher über einen[`Document`](../../document/) Wenn Sie einen Visitor über ein Glossary-Dokument ausführen möchten, müssen Sie[`Accept`](../../../aspose.words.buildingblocks/glossarydocument/accept/) .

## Beispiele

Zeigt Möglichkeiten zum Zugriff auf Bausteine in einem Glossardokument.

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

    // Es gibt verschiedene Möglichkeiten, auf Bausteine zuzugreifen.
    // 1 - Holen Sie sich die ersten/letzten Bausteine in der Sammlung:
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - Holen Sie sich einen Baustein nach Index:
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 - Holen Sie sich den ersten Baustein, der einer Galerie, einem Namen und einer Kategorie entspricht:
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // Wir werden das mit einem benutzerdefinierten Besucher tun,
    // Dadurch erhält jeder BuildingBlock im GlossaryDocument eine eindeutige GUID
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    // Besuchen Sie den Anfang/das Ende des Glossardokuments.
    glossaryDoc.Accept(visitor);
    // Besuchen Sie nur den Anfang des Glossardokuments.
    glossaryDoc.AcceptStart(visitor);
    // Besuchen Sie nur das Ende des Glossardokuments.
    glossaryDoc.AcceptEnd(visitor);
    Console.WriteLine(visitor.GetText());

    // In Microsoft Word können wir über „Einfügen“ -> „Schnellbausteine“ -> „Baustein-Organizer“ auf die Bausteine zugreifen.
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
* class [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/)
* class [DocumentVisitor](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
