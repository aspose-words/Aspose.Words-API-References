---
title: BuildingBlock
second_title: Aspose.Words für .NET-API-Referenz
description: Stellt einen Glossardokumenteintrag dar z. B. einen Baustein- AutoText- oder AutoKorrektur-Eintrag.
type: docs
weight: 120
url: /de/net/aspose.words.buildingblocks/buildingblock/
---
## BuildingBlock class

Stellt einen Glossardokumenteintrag dar, z. B. einen Baustein-, AutoText- oder AutoKorrektur-Eintrag.

```csharp
public class BuildingBlock : CompositeNode
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [BuildingBlock](buildingblock)(GlossaryDocument) | Initialisiert eine neue Instanz dieser Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Behavior](../../aspose.words.buildingblocks/buildingblock/behavior) { get; set; } | Gibt das Verhalten an, das angewendet werden soll, wenn der Inhalt des Bausteins in das Hauptdokument eingefügt wird. |
| [Category](../../aspose.words.buildingblocks/buildingblock/category) { get; set; } | Gibt die Kategorisierung der zweiten Ebene für den Baustein an. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Ruft alle unmittelbar untergeordneten Knoten dieses Knotens ab. |
| [Count](../../aspose.words/compositenode/count) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| [Description](../../aspose.words.buildingblocks/buildingblock/description) { get; set; } | Ruft die diesem Baustein zugeordnete Beschreibung ab oder legt sie fest. |
| virtual [Document](../../aspose.words/node/document) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FirstSection](../../aspose.words.buildingblocks/buildingblock/firstsection) { get; } | Ruft den ersten Abschnitt im Baustein ab. |
| [Gallery](../../aspose.words.buildingblocks/buildingblock/gallery) { get; set; } | Gibt die Kategorisierung der ersten Ebene für den Baustein zum Zweck der -Klassifizierung oder Sortierung der Benutzeroberfläche an. |
| [Guid](../../aspose.words.buildingblocks/buildingblock/guid) { get; set; } | Ruft eine Kennung (eine 128-Bit-GUID) ab oder legt sie fest, die diesen Baustein eindeutig identifiziert. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Gibt wahr zurück, wenn dieser Knoten untergeordnete Knoten hat. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Gibt wahr zurück, da dieser Knoten untergeordnete Knoten haben kann. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [LastSection](../../aspose.words.buildingblocks/buildingblock/lastsection) { get; } | Ruft den letzten Abschnitt im Baustein ab. |
| [Name](../../aspose.words.buildingblocks/buildingblock/name) { get; set; } | Ruft den Namen dieses Bausteins ab oder legt ihn fest. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words.buildingblocks/buildingblock/nodetype) { get; } | Gibt die zurückBuildingBlock wert. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Ruft den Knoten unmittelbar vor diesem Knoten ab. |
| [Range](../../aspose.words/node/range) { get; } | Gibt a zurück **Bereich** Objekt, das den Teil eines Dokuments darstellt, das in diesem Knoten enthalten ist. |
| [Sections](../../aspose.words.buildingblocks/buildingblock/sections) { get; } | Gibt eine Sammlung zurück, die alle Abschnitte im Baustein darstellt. |
| [Type](../../aspose.words.buildingblocks/buildingblock/type) { get; set; } | Gibt den Bausteintyp an. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/buildingblock/accept)(DocumentVisitor) | Akzeptiert einen Besucher. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [Clone](../../aspose.words/node/clone)(bool) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Reserviert für Systemnutzung. IXPfadNavigierbar. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Ruft den ersten Vorfahren der angegebenen ab[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Bietet Unterstützung für die Iteration für jeden Stil über die untergeordneten Knoten dieses Knotens. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Ruft den Text dieses Knotens und aller seiner Kinder ab. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knotenarray zurück. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ruft den nächsten Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ruft den vorherigen Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [Remove](../../aspose.words/node/remove)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag) Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Wählt eine Liste von Knoten aus, die mit dem XPath-Ausdruck übereinstimmen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Wählt den ersten Knoten aus, der mit dem XPath-Ausdruck übereinstimmt. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in einen String. |

### Bemerkungen

[`BuildingBlock`](../buildingblock) kann nur enthalten[`Section`](../../aspose.words/section) Knoten.

[`BuildingBlock`](../buildingblock) kann nur ein Kind von sein[`GlossaryDocument`](../glossarydocument).

Sie können neue Bausteine erstellen und sie in ein Glossardokument einfügen. Sie können vorhandene Bausteine ändern oder löschen. Sie können Bausteine zwischen Dokumenten kopieren oder verschieben. Sie können Inhalte eines Bausteins in ein Dokument einfügen.

Entspricht dem **docPart** , **docPartPr** und **docPartBody**Elemente in OOXML.

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

* class [CompositeNode](../../aspose.words/compositenode)
* namensraum [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
