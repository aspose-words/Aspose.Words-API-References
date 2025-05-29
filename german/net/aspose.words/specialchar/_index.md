---
title: SpecialChar Class
linktitle: SpecialChar
articleTitle: SpecialChar
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.SpecialChar, Ihr unverzichtbares Tool zur Verwaltung von Sonderzeichen in Dokumenten. Optimieren Sie Ihre Dokumentenverarbeitung noch heute!
type: docs
weight: 6950
url: /de/net/aspose.words/specialchar/
---
## SpecialChar class

Basisklasse für Sonderzeichen im Dokument.

Um mehr zu erfahren, besuchen Sie die[Aspose.Words Dokumentobjektmodell (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Dokumentationsartikel.

```csharp
public class SpecialChar : Inline
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
| override [Accept](../../aspose.words/specialchar/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Nimmt einen Besucher auf. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Erstellt ein Duplikat des Knotens. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Ruft den ersten Vorfahren des angegebenen[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ruft den ersten Vorgänger des angegebenen Objekttyps ab. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Ruft das Sonderzeichen ab, das dieser Knoten darstellt. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ruft den nächsten Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Ruft den vorherigen Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exportiert den Inhalt des Knotens in eine Zeichenfolge im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in eine Zeichenfolge. |

## Bemerkungen

Ein Microsoft Word-Dokument kann eine Reihe von Sonderzeichen enthalten, die Felder, Formularfelder, Formen, OLE-Objekte, Fußnoten usw. darstellen. Die Liste der Sonderzeichen finden Sie unter[`ControlChar`](../controlchar/).

`SpecialChar` ist ein Inline-Knoten und kann nur ein Kind von[`Paragraph`](../paragraph/).

`SpecialChar` char wird als Basisklasse für spezifischere Klassen verwendet, die Sonderzeichen darstellen, für die Aspose.Words programmgesteuerten Zugriff bereitstellt. Die`SpecialChar`Die Klasse wird auch selbst verwendet, um Sonderzeichen darzustellen, für die Aspose.Words keinen detaillierten programmgesteuerten Zugriff bietet.

## Beispiele

Zeigt, wie Sie mithilfe einer DocumentVisitor-Implementierung alle ausgeblendeten Inhalte aus einem Dokument entfernen.

```csharp
public void RemoveHiddenContentFromDocument()
{
    Document doc = new Document(MyDir + "Hidden content.docx");
    RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

    // Unten sind drei Arten von Feldern aufgeführt, die einen Dokumentbesucher akzeptieren können.
    // Dadurch kann es den akzeptierenden Knoten besuchen und dann seine untergeordneten Knoten in einer Tiefensuche durchlaufen.
    // 1 - Absatzknoten:
    Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 4, true);
    para.Accept(hiddenContentRemover);

    // 2 - Tabellenknoten:
    Table table = doc.FirstSection.Body.Tables[0];
    table.Accept(hiddenContentRemover);

    // 3 - Dokumentknoten:
    doc.Accept(hiddenContentRemover);

    doc.Save(ArtifactsDir + "Font.RemoveHiddenContentFromDocument.docx");
}

/// <summary>
/// Entfernt alle besuchten Knoten, die als „versteckter Inhalt“ markiert sind.
/// </summary>
public class RemoveHiddenContentVisitor : DocumentVisitor
{
    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein FieldStart-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        if (fieldStart.Font.Hidden)
            fieldStart.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein FieldEnd-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        if (fieldEnd.Font.Hidden)
            fieldEnd.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein FieldSeparator-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        if (fieldSeparator.Font.Hidden)
            fieldSeparator.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Run-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (run.Font.Hidden)
            run.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Absatzknoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        if (paragraph.ParagraphBreakFont.Hidden)
            paragraph.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein FormField gefunden wird.
    /// </summary>
    public override VisitorAction VisitFormField(FormField formField)
    {
        if (formField.Font.Hidden)
            formField.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument eine GroupShape gefunden wird.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        if (groupShape.Font.Hidden)
            groupShape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument eine Form gefunden wird.
    /// </summary>
    public override VisitorAction VisitShapeStart(Shape shape)
    {
        if (shape.Font.Hidden)
            shape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Kommentar gefunden wird.
    /// </summary>
    public override VisitorAction VisitCommentStart(Comment comment)
    {
        if (comment.Font.Hidden)
            comment.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument eine Fußnote gefunden wird.
    /// </summary>
    public override VisitorAction VisitFootnoteStart(Footnote footnote)
    {
        if (footnote.Font.Hidden)
            footnote.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Sonderzeichen gefunden wird.
    /// </summary>
    public override VisitorAction VisitSpecialChar(SpecialChar specialChar)
    {
        Console.WriteLine(specialChar.GetText());

        if (specialChar.Font.Hidden)
            specialChar.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn der Besuch eines Tabellenknotens im Dokument beendet ist.
    /// </summary>
    public override VisitorAction VisitTableEnd(Table table)
    {
        // Der Inhalt in Tabellenzellen kann das Flag für ausgeblendeten Inhalt haben, die Tabellen selbst jedoch nicht.
        // Wenn diese Tabelle nur versteckte Inhalte hätte, hätte dieser Besucher alles entfernt.
        // und es wären keine untergeordneten Knoten übrig.
        // Daher können wir auch die Tabelle selbst als versteckten Inhalt behandeln und entfernen.
        // Tabellen, die leer sind, aber keinen versteckten Inhalt haben, enthalten Zellen mit leeren Absätzen.
        // die dieser Besucher nicht entfernen wird.
        if (!table.HasChildNodes)
            table.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn der Besuch eines Zellknotens im Dokument beendet ist.
    /// </summary>
    public override VisitorAction VisitCellEnd(Cell cell)
    {
        if (!cell.HasChildNodes && cell.ParentNode != null)
            cell.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn der Besuch eines Zeilenknotens im Dokument beendet ist.
    /// </summary>
    public override VisitorAction VisitRowEnd(Row row)
    {
        if (!row.HasChildNodes && row.ParentNode != null)
            row.Remove();

        return VisitorAction.Continue;
    }
}
```

### Siehe auch

* class [Inline](../inline/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
