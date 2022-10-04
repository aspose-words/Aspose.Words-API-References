---
title: GlossaryDocument
second_title: Aspose.Words für .NET-API-Referenz
description: Stellt das Stammelement für ein Glossardokument innerhalb eines WordDokuments dar. Ein Glossardokument ist ein Speicher für AutoText AutoKorrekturEinträge und Bausteine.
type: docs
weight: 170
url: /de/net/aspose.words.buildingblocks/glossarydocument/
---
## GlossaryDocument class

Stellt das Stammelement für ein Glossardokument innerhalb eines Word-Dokuments dar. Ein Glossardokument ist ein Speicher für AutoText, AutoKorrektur-Einträge und Bausteine.

```csharp
public class GlossaryDocument : DocumentBase
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [GlossaryDocument](glossarydocument/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Ruft die Hintergrundform des Dokuments ab oder legt sie fest. Kann null sein. |
| [BuildingBlocks](../../aspose.words.buildingblocks/glossarydocument/buildingblocks/) { get; } | Gibt eine typisierte Auflistung zurück, die alle Bausteine im Glossardokument darstellt. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Ruft alle unmittelbar untergeordneten Knoten dieses Knotens ab. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| override [Document](../../aspose.words/documentbase/document/) { get; } |  |
| [FirstBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/firstbuildingblock/) { get; } | Ruft den ersten Baustein im Glossardokument ab. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Bietet Zugriff auf Eigenschaften von Schriftarten, die in diesem Dokument verwendet werden. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Gibt wahr zurück, wenn dieser Knoten untergeordnete Knoten hat. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Gibt wahr zurück, da dieser Knoten untergeordnete Knoten haben kann. |
| [LastBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/lastbuildingblock/) { get; } | Ruft den letzten Baustein im Glossardokument ab. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Bietet Zugriff auf die im Dokument verwendete Listenformatierung. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Wird aufgerufen, wenn ein Knoten im Dokument eingefügt oder entfernt wird. |
| override [NodeType](../../aspose.words.buildingblocks/glossarydocument/nodetype/) { get; } | Gibt die zurückGlossaryDocument wert. |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Holt oder setzt die Seitenfarbe des Dokuments. Diese Eigenschaft ist eine einfachere Version von[`BackgroundShape`](../../aspose.words/documentbase/backgroundshape/) . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten unmittelbar vor diesem Knoten ab. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt a zurück **Bereich** Objekt, das den Teil eines Dokuments darstellt, das in diesem Knoten enthalten ist. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Ermöglicht die Steuerung, wie externe Ressourcen geladen werden. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Gibt eine Sammlung von Stilen zurück, die im Dokument definiert sind. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Wird während verschiedener Dokumentverarbeitungsvorgänge aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Daten oder der Formatierung führen kann. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/glossarydocument/accept/)(DocumentVisitor) | Akzeptiert einen Besucher. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Reserviert für Systemnutzung. IXPfadNavigierbar. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Ruft den ersten Vorfahren der angegebenen ab[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| [GetBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/getbuildingblock/)(BuildingBlockGallery, string, string) | Findet einen Baustein anhand der angegebenen Galerie, Kategorie und des angegebenen Namens. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bietet Unterstützung für die Iteration für jeden Stil über die untergeordneten Knoten dieses Knotens. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ruft den Text dieses Knotens und aller seiner Kinder ab. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(Node, bool) | Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(Node, bool, ImportFormatMode) | Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument mit einer Option zur Steuerung der Formatierung. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knotenarray zurück. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ruft den nächsten Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ruft den vorherigen Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag/) Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Wählt eine Liste von Knoten aus, die mit dem XPath-Ausdruck übereinstimmen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Wählt den ersten Knoten aus, der mit dem XPath-Ausdruck übereinstimmt. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in einen String. |

### Bemerkungen

Einige Dokumente, normalerweise Vorlagen, können AutoText, AutoKorrektur-Einträge und/oder Bausteine (auch bekannt alsGlossar Dokumenteinträge ,Teile dokumentieren oderBausteine).

Um auf Bausteine zuzugreifen, müssen Sie ein Dokument in a laden[`Document`](../../aspose.words/document/) Objekt. Bausteine werden über verfügbar sein[`GlossaryDocument`](../../aspose.words/document/glossarydocument/) Eigentum.

[`GlossaryDocument`](./glossarydocument/) kann beliebig viele enthalten[`BuildingBlock`](../buildingblock/) Objekte. Jeder[`BuildingBlock`](../buildingblock/) stellt einen Dokumententeil dar.

Entspricht dem **GlossarDokument** und **docParts**Elemente in OOXML.

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

* class [DocumentBase](../../aspose.words/documentbase/)
* namensraum [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
