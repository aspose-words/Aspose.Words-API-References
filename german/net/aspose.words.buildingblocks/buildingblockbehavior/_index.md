---
title: BuildingBlockBehavior
second_title: Aspose.Words für .NET-API-Referenz
description: Gibt das Verhalten an das auf den Inhalt des Bausteins angewendet werden soll wenn er in das Hauptdokument eingefügt wird.
type: docs
weight: 130
url: /de/net/aspose.words.buildingblocks/buildingblockbehavior/
---
## BuildingBlockBehavior enumeration

Gibt das Verhalten an, das auf den Inhalt des Bausteins angewendet werden soll, wenn er in das Hauptdokument eingefügt wird.

```csharp
public enum BuildingBlockBehavior
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Content | `0` | Gibt an, dass der Baustein als Inline-Inhalt eingefügt werden soll. |
| Paragraph | `1` | Gibt an, dass der Baustein in einen eigenen Absatz eingefügt werden soll. |
| Page | `2` | Gibt an, dass der Baustein zu einer eigenen Seite hinzugefügt werden soll. |
| Default | `0` | Gleich wieContent . |

### Bemerkungen

Entspricht dem **ST_DocPartBehavior** Geben Sie OOXML ein.

### Beispiele

Zeigt, wie Sie einem Dokument einen benutzerdefinierten Baustein hinzufügen.

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

    // Alle neuen Baustein-GUIDs haben standardmäßig denselben Nullwert, und wir können ihnen einen neuen eindeutigen Wert zuweisen.
    Assert.AreEqual("00000000-0000-0000-0000-000000000000", block.Guid.ToString());

    block.Guid = Guid.NewGuid();

    // Die folgenden Eigenschaften kategorisieren Bausteine
    // im Menü können wir in Microsoft Word über "Einfügen" -> "Schnelle Teile" -> "Baustein-Organizer".
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

    // Bevor wir diesen Baustein zu unserem Dokument hinzufügen können, müssen wir ihm einige Inhalte geben,
    // was wir mit einem Dokumentenbesucher tun werden. Dieser Besucher legt auch eine Kategorie, eine Galerie und ein Verhalten fest.
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    block.Accept(visitor);

    // Wir können auf den Block zugreifen, den wir gerade aus dem Glossardokument erstellt haben.
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

    // Der Block selbst ist ein Abschnitt, der den Text enthält.
    Assert.AreEqual($"Text inside {customBlock.Name}\f", customBlock.FirstSection.Body.FirstParagraph.GetText());
    Assert.AreEqual(customBlock.FirstSection, customBlock.LastSection);

    // Jetzt können wir es als neuen Abschnitt in das Dokument einfügen.
    doc.AppendChild(doc.ImportNode(customBlock.FirstSection, true));

    // Wir können es auch im Building Blocks Organizer von Microsoft Word finden und manuell platzieren.
    doc.Save(ArtifactsDir + "BuildingBlocks.CreateAndInsert.dotx");
}

/// <summary>
/// Richtet einen besuchten Baustein ein, der als schneller Teil in das Dokument eingefügt wird, und fügt seinem Inhalt Text hinzu.
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
        // Konfigurieren Sie den Baustein als Schnellteil und fügen Sie Eigenschaften hinzu, die von Building Blocks Organizer verwendet werden.
        block.Behavior = BuildingBlockBehavior.Paragraph;
        block.Category = "My custom building blocks";
        block.Description =
            "Using this block in the Quick Parts section of word will place its contents at the cursor.";
        block.Gallery = BuildingBlockGallery.QuickParts;

        // Abschnitt mit Text hinzufügen.
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

* namensraum [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
