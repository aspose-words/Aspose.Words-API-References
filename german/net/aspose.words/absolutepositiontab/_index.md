---
title: AbsolutePositionTab Class
linktitle: AbsolutePositionTab
articleTitle: AbsolutePositionTab
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.AbsolutePositionTab, die eine präzise Textpositionierung in WordprocessingML für eine verbesserte Dokumentformatierung und -kontrolle ermöglicht.
type: docs
weight: 120
url: /de/net/aspose.words/absolutepositiontab/
---
## AbsolutePositionTab class

Ein Tabulator mit absoluter Position ist ein Zeichen, das verwendet wird, um die Position in der aktuellen Textzeile beim Anzeigen dieses WordprocessingML-Inhalts nach vorne zu verschieben.

Um mehr zu erfahren, besuchen Sie die[Aspose.Words Dokumentobjektmodell (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Dokumentationsartikel.

```csharp
public class AbsolutePositionTab : SpecialChar
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [Font](../../aspose.words/inline/font/) { get; } | Bietet Zugriff auf die Schriftformatierung dieses Objekts. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Rückgaben`WAHR` wenn dieser Knoten andere Knoten enthalten kann. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Gibt „true“ zurück, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Änderungsverfolgung aktiviert war. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Rückgaben`WAHR` wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Rückgaben`WAHR` wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words/specialchar/nodetype/) { get; } | RückgabenSpecialChar . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Ruft das übergeordnete Element ab[`Paragraph`](../paragraph/) dieses Knotens. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorausgeht. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt einen[`Range`](../range/)Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words/absolutepositiontab/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Nimmt einen Besucher auf. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Erstellt ein Duplikat des Knotens. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Ruft den ersten Vorfahren des angegebenen[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ruft den ersten Vorgänger des angegebenen Objekttyps ab. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Ruft das Sonderzeichen ab, das dieser Knoten darstellt. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ruft den nächsten Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Ruft den vorherigen Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exportiert den Inhalt des Knotens in eine Zeichenfolge im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in eine Zeichenfolge. |

## Beispiele

Zeigt, wie Tabulatorzeichen mit absoluter Position mit einem Dokumentbesucher verarbeitet werden.

```csharp
public void DocumentToTxt()
{
    Document doc = new Document(MyDir + "Absolute position tab.docx");

    // Extrahieren Sie den Textinhalt unseres Dokuments, indem Sie diesen benutzerdefinierten Dokumentbesucher akzeptieren.
    DocTextExtractor myDocTextExtractor = new DocTextExtractor();
    Section fisrtSection = doc.FirstSection;
    fisrtSection.Body.Accept(myDocTextExtractor);
    // Besuchen Sie nur den Anfang des Dokumenttexts.
    fisrtSection.Body.AcceptStart(myDocTextExtractor);
    // Besuchen Sie nur das Ende des Dokumenttexts.
    fisrtSection.Body.AcceptEnd(myDocTextExtractor);

    // Die absolute Position Tab, für die es kein Äquivalent in Stringform gibt, wurde explizit in ein Tabulatorzeichen umgewandelt.
    Assert.AreEqual("Before AbsolutePositionTab\tAfter AbsolutePositionTab", myDocTextExtractor.GetText());

    // Ein AbsolutePositionTab kann auch selbst einen DocumentVisitor akzeptieren.
    AbsolutePositionTab absPositionTab = (AbsolutePositionTab)doc.FirstSection.Body.FirstParagraph.GetChild(NodeType.SpecialChar, 0, true);

    myDocTextExtractor = new DocTextExtractor();
    absPositionTab.Accept(myDocTextExtractor);

    Assert.AreEqual("\t", myDocTextExtractor.GetText());
}

/// <summary>
/// Sammelt den Textinhalt aller Läufe im besuchten Dokument. Ersetzt alle absoluten Tabulatorzeichen durch normale Tabulatoren.
/// </summary>
public class DocTextExtractor : DocumentVisitor
{
    public DocTextExtractor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Run-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        AppendText(run.Text);
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein AbsolutePositionTab-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
    {
        mBuilder.Append("\t");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Fügt der aktuellen Ausgabe Text hinzu. Beachtet das aktivierte/deaktivierte Ausgabeflag.
    /// </summary>
    private void AppendText(string text)
    {
        mBuilder.Append(text);
    }

    /// <summary>
    /// Klartext des vom Besucher gesammelten Dokuments.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### Siehe auch

* class [SpecialChar](../specialchar/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
