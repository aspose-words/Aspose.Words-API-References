---
title: BuildingBlock.AcceptStart
linktitle: AcceptStart
articleTitle: AcceptStart
second_title: Aspose.Words für .NET
description: Entdecken Sie die BuildingBlock AcceptStart-Methode, heißen Sie Besucher nahtlos willkommen und verbessern Sie ihr Erlebnis vom Moment ihrer Ankunft an.
type: docs
weight: 150
url: /de/net/aspose.words.buildingblocks/buildingblock/acceptstart/
---
## BuildingBlock.AcceptStart method

Akzeptiert einen Besucher für den Besuch des Anfangs des BuildingBlocks.

```csharp
public override VisitorAction AcceptStart(DocumentVisitor visitor)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| visitor | DocumentVisitor | Der Dokumentbesucher. |

### Rückgabewert

Die vom Besucher auszuführende Aktion.

## Beispiele

Zeigt, wie einem Dokument ein benutzerdefinierter Baustein hinzugefügt wird.

```csharp
public void CreateAndInsert()
{
    // Das Glossardokument eines Dokuments speichert Bausteine.
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();
    doc.GlossaryDocument = glossaryDoc;

    // Erstellen Sie einen Baustein, benennen Sie ihn und fügen Sie ihn dann dem Glossardokument hinzu.
    BuildingBlock block = new BuildingBlock(glossaryDoc)
    {
        Name = "Custom Block"
    };

    glossaryDoc.AppendChild(block);

    // Alle neuen Baustein-GUIDs haben standardmäßig denselben Nullwert und wir können ihnen einen neuen eindeutigen Wert zuweisen.
    Assert.AreEqual("00000000-0000-0000-0000-000000000000", block.Guid.ToString());

    block.Guid = Guid.NewGuid();

    // Die folgenden Eigenschaften kategorisieren Bausteine
    // Im Menü können wir in Microsoft Word über „Einfügen“ -> „Schnellbausteine“ -> „Baustein-Organizer“ darauf zugreifen.
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

    // Bevor wir diesen Baustein zu unserem Dokument hinzufügen können, müssen wir ihm einen Inhalt geben,
    // Dies tun wir mithilfe eines Dokumentbesuchers. Dieser Besucher legt auch eine Kategorie, eine Galerie und ein Verhalten fest.
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    // Besuchen Sie den Anfang/das Ende des BuildingBlocks.
    block.Accept(visitor);

    // Wir können auf den Block zugreifen, den wir gerade aus dem Glossardokument erstellt haben.
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

    // Der Block selbst ist ein Abschnitt, der den Text enthält.
    Assert.AreEqual($"Text inside {customBlock.Name}\f", customBlock.FirstSection.Body.FirstParagraph.GetText());
    Assert.AreEqual(customBlock.FirstSection, customBlock.LastSection);
    // Jetzt können wir es als neuen Abschnitt in das Dokument einfügen.
    doc.AppendChild(doc.ImportNode(customBlock.FirstSection, true));

    // Wir können es auch im Baustein-Organizer von Microsoft Word finden und manuell platzieren.
    doc.Save(ArtifactsDir + "BuildingBlocks.CreateAndInsert.dotx");
}

/// <summary>
/// Richtet einen besuchten Baustein zum Einfügen in das Dokument als Schnellbaustein ein und fügt seinem Inhalt Text hinzu.
/// </summary>
public class BuildingBlockVisitor : DocumentVisitor
{
    public BuildingBlockVisitor(GlossaryDocument ownerGlossaryDoc)
    {
        mBuilder = new StringBuilder();
        mGlossaryDoc = ownerGlossaryDoc;
    }

    public override VisitorAction VisitBuildingBlockStart(BuildingBlock block)
    {
        // Konfigurieren Sie den Baustein als Schnellbaustein und fügen Sie Eigenschaften hinzu, die vom Building Blocks Organizer verwendet werden.
        block.Behavior = BuildingBlockBehavior.Paragraph;
        block.Category = "My custom building blocks";
        block.Description =
            "Using this block in the Quick Parts section of word will place its contents at the cursor.";
        block.Gallery = BuildingBlockGallery.QuickParts;

        // Einen Abschnitt mit Text hinzufügen.
        // Durch das Einfügen des Blocks in das Dokument wird dieser Abschnitt mit seinen untergeordneten Knoten an der Position angehängt.
        Section section = new Section(mGlossaryDoc);
        block.AppendChild(section);
        block.FirstSection.EnsureMinimum();

        Run run = new Run(mGlossaryDoc, "Text inside " + block.Name);
        block.FirstSection.Body.FirstParagraph.AppendChild(run);

        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockEnd(BuildingBlock block)
    {
        mBuilder.Append("Visited " + block.Name + "\r\n");
        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
    private readonly GlossaryDocument mGlossaryDoc;
}
```

### Siehe auch

* enum [VisitorAction](../../../aspose.words/visitoraction/)
* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [BuildingBlock](../)
* namensraum [Aspose.Words.BuildingBlocks](../../../aspose.words.buildingblocks/)
* Montage [Aspose.Words](../../../)
