---
title: AbsolutePositionTab
second_title: Aspose.Words für .NET-API-Referenz
description: Ein absoluter Positionstabulator ist ein Zeichen das verwendet wird um die Position in der aktuellen Textzeile vorzurücken wenn dieser WordprocessingMLInhalt angezeigt wird.
type: docs
weight: 10
url: /de/net/aspose.words/absolutepositiontab/
---
## AbsolutePositionTab class

Ein absoluter Positionstabulator ist ein Zeichen, das verwendet wird, um die Position in der aktuellen Textzeile vorzurücken, wenn dieser WordprocessingML-Inhalt angezeigt wird.

```csharp
public class AbsolutePositionTab : SpecialChar
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [Font](../../aspose.words/inline/font/) { get; } | Bietet Zugriff auf die Schriftformatierung dieses Objekts. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Gibt wahr zurück, wenn dieser Knoten andere Knoten enthalten kann. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsnachverfolgung aktiviert war. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Gibt „true“ zurück, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Änderungsverfolgung aktiviert war. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | gibt zurück **Stimmt** wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsnachverfolgung aktiviert war. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | gibt zurück **Stimmt** wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsnachverfolgung aktiviert war. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words/specialchar/nodetype/) { get; } | gibt zurück **NodeType.SpecialChar** . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Ruft das übergeordnete Element ab[`Paragraph`](../paragraph/) dieses Knotens. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten unmittelbar vor diesem Knoten ab. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt a zurück **Bereich** Objekt, das den Teil eines Dokuments darstellt, das in diesem Knoten enthalten ist. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words/absolutepositiontab/accept/)(DocumentVisitor) | Akzeptiert einen Besucher. |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Ruft den ersten Vorfahren der angegebenen ab[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Ruft das Sonderzeichen ab, das dieser Knoten darstellt. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ruft den nächsten Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ruft den vorherigen Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in einen String. |

### Beispiele

Zeigt, wie Tabulatorzeichen mit absoluter Position mit einem Dokumentbesucher verarbeitet werden.

```csharp
public void DocumentToTxt()
{
    Document doc = new Document(MyDir + "Absolute position tab.docx");

    // Extrahieren Sie den Textinhalt unseres Dokuments, indem Sie diesen benutzerdefinierten Dokumentbesucher akzeptieren.
    DocTextExtractor myDocTextExtractor = new DocTextExtractor();
    doc.FirstSection.Body.Accept(myDocTextExtractor);

    // Die absolute Position tab, die kein Äquivalent in Zeichenfolgenform hat, wurde explizit in ein Tabulatorzeichen umgewandelt.
    Assert.AreEqual("Before AbsolutePositionTab\tAfter AbsolutePositionTab", myDocTextExtractor.GetText());

    // Ein AbsolutePositionTab kann auch selbst einen DocumentVisitor akzeptieren.
    AbsolutePositionTab absPositionTab = (AbsolutePositionTab)doc.FirstSection.Body.FirstParagraph.GetChild(NodeType.SpecialChar, 0, true);

    myDocTextExtractor = new DocTextExtractor();
    absPositionTab.Accept(myDocTextExtractor);

    Assert.AreEqual("\t", myDocTextExtractor.GetText());
}

/// <summary>
/// Sammelt den Textinhalt aller Läufe im besuchten Dokument. Ersetzt alle absoluten Tabulatorzeichen durch gewöhnliche Tabulatoren.
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
    /// Fügt Text zur aktuellen Ausgabe hinzu. Berücksichtigt das aktivierte/deaktivierte Ausgangsflag.
    /// </summary>
    private void AppendText(string text)
    {
        mBuilder.Append(text);
    }

    /// <summary>
    /// Klartext des Dokuments, das vom Besucher gesammelt wurde.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
