---
title: BuildingBlock Class
linktitle: BuildingBlock
articleTitle: BuildingBlock
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.BuildingBlocks.BuildingBlock zum Erstellen und Verwalten von Glossareinträgen wie AutoText und AutoKorrektur für eine verbesserte Dokumenteffizienz.
type: docs
weight: 320
url: /de/net/aspose.words.buildingblocks/buildingblock/
---
## BuildingBlock class

Stellt einen Glossardokumenteintrag dar, z. B. einen Baustein-, AutoText- oder AutoKorrektur-Eintrag.

Um mehr zu erfahren, besuchen Sie die[Aspose.Words Dokumentobjektmodell (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Dokumentationsartikel.

```csharp
public class BuildingBlock : CompositeNode
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [BuildingBlock](buildingblock/)(*[GlossaryDocument](../glossarydocument/)*) | Initialisiert eine neue Instanz dieser Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Behavior](../../aspose.words.buildingblocks/buildingblock/behavior/) { get; set; } | Gibt das Verhalten an, das angewendet werden soll, wenn der Inhalt des Bausteins in das Hauptdokument eingefügt wird. |
| [Category](../../aspose.words.buildingblocks/buildingblock/category/) { get; set; } | Gibt die Kategorisierung der zweiten Ebene für den Baustein an. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbar untergeordneten Elemente dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| [Description](../../aspose.words.buildingblocks/buildingblock/description/) { get; set; } | Ruft die mit diesem Baustein verknüpfte Beschreibung ab oder legt sie fest. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FirstSection](../../aspose.words.buildingblocks/buildingblock/firstsection/) { get; } | Ruft den ersten Abschnitt im Baustein ab. |
| [Gallery](../../aspose.words.buildingblocks/buildingblock/gallery/) { get; set; } | Gibt die Kategorisierung der ersten Ebene für den Baustein zum Zwecke der Klassifizierung oder der Sortierung der Benutzeroberfläche an. |
| [Guid](../../aspose.words.buildingblocks/buildingblock/guid/) { get; set; } | Ruft einen Bezeichner (eine 128-Bit-GUID) ab oder legt ihn fest, der diesen Baustein eindeutig identifiziert. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Rückgaben`WAHR` wenn dieser Knoten untergeordnete Knoten hat. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Rückgaben`WAHR` da dieser Knoten untergeordnete Knoten haben kann. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [LastSection](../../aspose.words.buildingblocks/buildingblock/lastsection/) { get; } | Ruft den letzten Abschnitt im Baustein ab. |
| [Name](../../aspose.words.buildingblocks/buildingblock/name/) { get; set; } | Ruft den Namen dieses Bausteins ab oder legt ihn fest. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words.buildingblocks/buildingblock/nodetype/) { get; } | Gibt dieBuildingBlock Wert. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorausgeht. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt einen[`Range`](../../aspose.words/range/)Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [Sections](../../aspose.words.buildingblocks/buildingblock/sections/) { get; } | Gibt eine Sammlung zurück, die alle Abschnitte im Baustein darstellt. |
| [Type](../../aspose.words.buildingblocks/buildingblock/type/) { get; set; } | Gibt den Bausteintyp an. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/buildingblock/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Nimmt einen Besucher auf. |
| override [AcceptEnd](../../aspose.words.buildingblocks/buildingblock/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Akzeptiert einen Besucher für den Besuch des Endes des BuildingBlocks. |
| override [AcceptStart](../../aspose.words.buildingblocks/buildingblock/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Akzeptiert einen Besucher für den Besuch des Anfangs des BuildingBlocks. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Erstellt einen Navigator, der zum Durchlaufen und Lesen von Knoten verwendet werden kann. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Ruft den ersten Vorfahren des angegebenen[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ruft den ersten Vorgänger des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bietet Unterstützung für die Iteration des For-Each-Stils über die untergeordneten Knoten dieses Knotens. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ruft den Text dieses Knotens und aller seiner untergeordneten Knoten ab. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knoten-Array zurück. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ruft den nächsten Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ruft den vorherigen Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag/) Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Wählt den ersten[`Node`](../../aspose.words/node/) das dem XPath-Ausdruck entspricht. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exportiert den Inhalt des Knotens in eine Zeichenfolge im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in eine Zeichenfolge. |

## Bemerkungen

`BuildingBlock` kann nur enthalten[`Section`](../../aspose.words/section/) Knoten.

`BuildingBlock` kann nur ein Kind sein von[`GlossaryDocument`](../glossarydocument/).

Sie können neue Bausteine erstellen und in ein Glossardokument einfügen. Sie können vorhandene Bausteine ändern oder löschen. Sie können Bausteine zwischen Dokumenten kopieren oder verschieben. Sie können den Inhalt eines Bausteins in ein Dokument einfügen.

Entspricht dem**docPart** ,**docPartPr** Und**docPartBody**Elemente in OOXML.

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

* class [CompositeNode](../../aspose.words/compositenode/)
* namensraum [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* Montage [Aspose.Words](../../)
