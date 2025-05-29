---
title: BuildingBlockType Enum
linktitle: BuildingBlockType
articleTitle: BuildingBlockType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words BuildingBlockType-Aufzählung, um die Dokumentfunktionalität in Microsoft Word zu verbessern. Schalten Sie einzigartige Sichtbarkeit und Verhalten von Bausteinen frei!
type: docs
weight: 360
url: /de/net/aspose.words.buildingblocks/buildingblocktype/
---
## BuildingBlockType enumeration

Gibt einen Bausteintyp an. Der Typ kann die Sichtbarkeit und das Verhalten des Bausteins in Microsoft Word beeinflussen.

```csharp
public enum BuildingBlockType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Für den Baustein sind keine Typinformationen angegeben. |
| AutomaticallyReplaceNameWithContent | `1` | Ermöglicht das automatische Einfügen des Bausteins in das Dokument, wenn sein Name in eine Anwendung eingegeben wird. |
| StructuredDocumentTagPlaceholderText | `2` | Der Baustein ist ein strukturierter Platzhaltertext für Dokument-Tags. |
| FormFieldHelpText | `3` | Der Baustein ist ein Hilfetext für ein Formularfeld. |
| Normal | `4` | Der Baustein ist ein normaler (also regulärer) Glossar-Dokumenteintrag. |
| AutoCorrect | `5` | Der Baustein ist mit den Rechtschreib- und Grammatiktools verknüpft. |
| AutoText | `6` | Der Baustein ist ein AutoText-Eintrag. |
| All | `7` | Der Baustein ist mit allen Typen verknüpft. |
| Default | `0` | Speichern unterNone . |

## Bemerkungen

Entspricht dem**ST_DocPartType** Geben Sie OOXML ein.

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

* namensraum [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* Montage [Aspose.Words](../../)
