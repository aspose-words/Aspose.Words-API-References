---
title: FieldStart Class
linktitle: FieldStart
articleTitle: FieldStart
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.FieldStart, Ihren Schlüssel zur effizienten Verwaltung von Word-Feldern in Dokumenten. Optimieren Sie noch heute Ihre Dokumentenverarbeitung!
type: docs
weight: 2840
url: /de/net/aspose.words.fields/fieldstart/
---
## FieldStart class

Stellt den Anfang eines Word-Felds in einem Dokument dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldStart : FieldChar
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [FieldData](../../aspose.words.fields/fieldstart/fielddata/) { get; } | Ruft benutzerdefinierte Felddaten ab, die mit dem Feld verknüpft sind. |
| [FieldType](../../aspose.words.fields/fieldchar/fieldtype/) { get; } | Gibt den Typ des Felds zurück. |
| [Font](../../aspose.words/inline/font/) { get; } | Bietet Zugriff auf die Schriftformatierung dieses Objekts. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Rückgaben`WAHR` wenn dieser Knoten andere Knoten enthalten kann. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war. |
| [IsDirty](../../aspose.words.fields/fieldchar/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Gibt „true“ zurück, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Änderungsverfolgung aktiviert war. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [IsLocked](../../aspose.words.fields/fieldchar/islocked/) { get; set; } | Ruft ab oder legt fest, ob das übergeordnete Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Rückgaben`WAHR` wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Rückgaben`WAHR` wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words.fields/fieldstart/nodetype/) { get; } | RückgabenFieldStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Ruft das übergeordnete Element ab[`Paragraph`](../../aspose.words/paragraph/) dieses Knotens. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorausgeht. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt einen[`Range`](../../aspose.words/range/)Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words.fields/fieldstart/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Nimmt einen Besucher auf. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Erstellt ein Duplikat des Knotens. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Ruft den ersten Vorfahren des angegebenen[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ruft den ersten Vorgänger des angegebenen Objekttyps ab. |
| [GetField](../../aspose.words.fields/fieldchar/getfield/)() | Gibt ein Feld für das Feld char zurück. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Ruft das Sonderzeichen ab, das dieser Knoten darstellt. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ruft den nächsten Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ruft den vorherigen Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exportiert den Inhalt des Knotens in eine Zeichenfolge im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in eine Zeichenfolge. |

## Bemerkungen

`FieldStart` ist ein Inline-Level-Knoten und wird durch the dargestellt[`FieldStartChar`](../../aspose.words/controlchar/fieldstartchar/) Steuerzeichen im Dokument.

`FieldStart` kann nur ein Kind sein von[`Paragraph`](../../aspose.words/paragraph/).

Ein vollständiges Feld in einem Microsoft Word-Dokument ist eine komplexe Struktur, die aus einem Feldstartzeichen, einem Feldcode, einem Feldtrennzeichen, einem Feldergebniszeichen und einem Feldendezeichen besteht. Einige Felder verfügen nur über Feldstart, Feldcode und Feldende.

Um einfach ein neues Feld in ein Dokument einzufügen, verwenden Sie die[`InsertField`](../../aspose.words/documentbuilder/insertfield/) -Methode.

## Beispiele

Zeigt, wie mit einer Sammlung von Feldern gearbeitet wird.

```csharp
public void FieldCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
    builder.InsertField(" TIME ");
    builder.InsertField(" REVNUM ");
    builder.InsertField(" AUTHOR  \"John Doe\" ");
    builder.InsertField(" SUBJECT \"My Subject\" ");
    builder.InsertField(" QUOTE \"Hello world!\" ");
    doc.UpdateFields();

    FieldCollection fields = doc.Range.Fields;

    Assert.AreEqual(6, fields.Count);

    // Durchlaufen Sie die Feldsammlung und drucken Sie Inhalt und Typ
    // jedes Felds mithilfe einer benutzerdefinierten Besucherimplementierung.
    FieldVisitor fieldVisitor = new FieldVisitor();

    using (IEnumerator<Field> fieldEnumerator = fields.GetEnumerator())
    {
        while (fieldEnumerator.MoveNext())
        {
            if (fieldEnumerator.Current != null)
            {
                fieldEnumerator.Current.Start.Accept(fieldVisitor);
                fieldEnumerator.Current.Separator?.Accept(fieldVisitor);
                fieldEnumerator.Current.End.Accept(fieldVisitor);
            }
            else
            {
                Console.WriteLine("There are no fields in the document.");
            }
        }
    }

    Console.WriteLine(fieldVisitor.GetText());
}

/// <summary>
/// Dokumentieren Sie die Besucherimplementierung, die Feldinformationen druckt.
/// </summary>
public class FieldVisitor : DocumentVisitor
{
    public FieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Ruft den Klartext des vom Besucher gesammelten Dokuments ab.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein FieldStart-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        mBuilder.AppendLine("Found field: " + fieldStart.FieldType);
        mBuilder.AppendLine("\tField code: " + fieldStart.GetField().GetFieldCode());
        mBuilder.AppendLine("\tDisplayed as: " + fieldStart.GetField().Result);

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein FieldSeparator-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein FieldEnd-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mBuilder.AppendLine("End of field: " + fieldEnd.FieldType);

        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

Zeigt, wie Sie alle Hyperlinks in einem Word-Dokument finden und dann deren URLs und Anzeigenamen ändern.

```csharp
using System;
using System.Linq;
using System.Text;
using System.Text.RegularExpressions;
using Aspose.Words;
using Aspose.Words.Fields;
using NUnit.Framework;

namespace ApiExamples
{
    public class ExReplaceHyperlinks : ApiExampleBase
    {
        public void Fields()
        {
            Document doc = new Document(MyDir + "Hyperlinks.docx");

            // Hyperlinks in Word-Dokumenten sind Felder. Um mit der Suche nach Hyperlinks zu beginnen, müssen wir zunächst alle Felder finden.
            // Verwenden Sie die Methode „SelectNodes“, um alle Felder im Dokument über einen XPath zu finden.
            NodeList fieldStarts = doc.SelectNodes("//FeldStart");

            foreach (FieldStart fieldStart in fieldStarts.OfType<FieldStart>())
            {
                if (fieldStart.FieldType == FieldType.FieldHyperlink)
                {
                    Hyperlink hyperlink = new Hyperlink(fieldStart);

                    // Hyperlinks, die auf Lesezeichen verweisen, haben keine URLs.
                    if (hyperlink.IsLocal)
                        continue;

                    // Geben Sie jedem URL-Hyperlink eine neue URL und einen neuen Namen.
                    hyperlink.Target = NewUrl;
                    hyperlink.Name = NewName;
                }
            }

            doc.Save(ArtifactsDir + "ReplaceHyperlinks.Fields.docx");
        }

        private const string NewUrl = @"http://www.aspose.com";
        private const string NewName = "Aspose - The .NET & Java Component Publisher";
    }

              /// <Zusammenfassung>
                  /// HYPERLINK-Felder enthalten und zeigen Hyperlinks im Dokumenttext an. Ein Feld in Aspose.Words
                  /// besteht aus mehreren Knoten und es kann schwierig sein, direkt mit all diesen Knoten zu arbeiten.
              /// Diese Implementierung funktioniert nur, wenn der Hyperlink-Code und der Name jeweils nur aus einem Run-Knoten bestehen.
             ///
              /// Die Knotenstruktur für Felder ist wie folgt:
              ///
              /// [FeldStart][Ausführen - Feldcode][FeldTrennzeichen][Ausführen - Feldergebnis][FeldEnde]
              ///
              /// Nachfolgend sind zwei Beispielfeldcodes für HYPERLINK-Felder aufgeführt:
              /// HYPERLINK "URL"
              /// HYPERLINK \l "Lesezeichenname"
              ///
              /// Die Eigenschaft „Ergebnis“ eines Felds enthält Text, den das Feld dem Benutzer im Dokumenttext anzeigt.
              /// </Zusammenfassung>
    internal class Hyperlink
    {
        internal Hyperlink(FieldStart fieldStart)
        {
            if (fieldStart == null)
                throw new ArgumentNullException("fieldStart");
            if (fieldStart.FieldType != FieldType.FieldHyperlink)
                throw new ArgumentException("Field start type must be FieldHyperlink.");

            mFieldStart = fieldStart;

            // Suchen Sie den Feldtrennknoten.
            mFieldSeparator = FindNextSibling(mFieldStart, NodeType.FieldSeparator);
            if (mFieldSeparator == null)
                throw new InvalidOperationException("Cannot find field separator.");

                // Normalerweise können wir den Endknoten des Feldes immer finden, aber das Beispieldokument
                // enthält einen Absatzumbruch innerhalb eines Hyperlinks, der das Feldende
                // im nächsten Absatz. Es wird viel komplizierter sein, Felder zu behandeln, die sich über mehrere
            // Absätze korrekt. In diesem Fall reicht es aus, das Feldende auf null zu setzen.
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

            // Der Feldcode sieht etwa so aus: „HYPERLINK „http:\\www.myurl.com““, kann aber aus mehreren Durchläufen bestehen.
            string fieldCode = GetTextSameParent(mFieldStart.NextSibling, mFieldSeparator);
            Match match = gRegex.Match(fieldCode.Trim());

            // Der Hyperlink ist lokal, wenn \l im Feldcode vorhanden ist.
            mIsLocal = match.Groups[1].Length > 0; 
            mTarget = match.Groups[2].Value;
        }

                  /// <Zusammenfassung>
                  /// Ruft den Anzeigenamen des Hyperlinks ab oder legt ihn fest.
                  /// </Zusammenfassung>
        internal string Name
        {
            get
            {
                return GetTextSameParent(mFieldSeparator, mFieldEnd);
            }
            set
            {
                    // Der Anzeigename des Hyperlinks wird im Feldergebnis gespeichert, das ein Run ist
                // Knoten zwischen Feldtrennzeichen und Feldende.
                Run fieldResult = (Run) mFieldSeparator.NextSibling;
                fieldResult.Text = value;

                // Wenn das Feldergebnis aus mehreren Durchläufen besteht, diese Durchläufe löschen.
                RemoveSameParent(fieldResult.NextSibling, mFieldEnd);
            }
        }

                  /// <Zusammenfassung>
                  /// Ruft die Ziel-URL oder den Lesezeichennamen des Hyperlinks ab oder legt diese fest.
                  /// </Zusammenfassung>
        internal string Target
        {
            get
            {
                return mTarget;
            }
            set
            {
                mTarget = value;
                UpdateFieldCode();
            }
        }

                  /// <Zusammenfassung>
                  /// Wahr, wenn das Ziel des Hyperlinks ein Lesezeichen innerhalb des Dokuments ist. Falsch, wenn der Hyperlink eine URL ist.
                  /// </Zusammenfassung>
        internal bool IsLocal
        {
            get
            {
                return mIsLocal;
            }
            set
            {
                mIsLocal = value;
                UpdateFieldCode();
            }
        }

        private void UpdateFieldCode()
        {
            // Der Feldcode eines Felds befindet sich in einem Run-Knoten zwischen dem Startknoten und dem Feldtrennzeichen des Felds.
            Run fieldCode = (Run) mFieldStart.NextSibling;
            fieldCode.Text = string.Format("HYPERLINK {0}\"{1}\"", ((mIsLocal) ? "\\l " : ""), mTarget);

            // Wenn der Feldcode aus mehr als einem Lauf besteht, löschen Sie diese Läufe.
            RemoveSameParent(fieldCode.NextSibling, mFieldSeparator);
        }

                  /// <Zusammenfassung>
                  /// Durchläuft die Geschwister beginnend beim Startknoten, bis ein Knoten des angegebenen Typs oder Null gefunden wird.
                  /// </Zusammenfassung>
        private static Node FindNextSibling(Node startNode, NodeType nodeType)
        {
            for (Node node = startNode; node != null; node = node.NextSibling)
            {
                if (node.NodeType == nodeType)
                    return node;
            }

            return null;
        }

                  /// <Zusammenfassung>
                  /// Ruft Text vom Anfangs- bis zum Endknoten ab, jedoch nicht einschließlich des Endknotens.
                  /// </Zusammenfassung>
        private static string GetTextSameParent(Node startNode, Node endNode)
        {
            if ((endNode != null) && (startNode.ParentNode != endNode.ParentNode))
                throw new ArgumentException("Start and end nodes are expected to have the same parent.");

            StringBuilder builder = new StringBuilder();
            for (Node child = startNode; !child.Equals(endNode); child = child.NextSibling)
                builder.Append(child.GetText());

            return builder.ToString();
        }

                  /// <Zusammenfassung>
                  /// Entfernt Knoten vom Start- bis zum Endknoten, jedoch nicht einschließlich des Endknotens.
                  /// Setzt voraus, dass Start- und Endknoten denselben übergeordneten Knoten haben.
                  /// </Zusammenfassung>
        private static void RemoveSameParent(Node startNode, Node endNode)
        {
            if (endNode != null && startNode.ParentNode != endNode.ParentNode)
                throw new ArgumentException("Start and end nodes are expected to have the same parent.");

            Node curChild = startNode;
            while ((curChild != null) && (curChild != endNode))
            {
                Node nextChild = curChild.NextSibling;
                curChild.Remove();
                curChild = nextChild;
            }
        }

        private readonly Node mFieldStart;
        private readonly Node mFieldSeparator;
        private readonly Node mFieldEnd;
        private bool mIsLocal;
        private string mTarget;

        private static readonly Regex gRegex = new Regex(
            "\\S+" + // Ein oder mehrere HYPERLINKs ohne Leerzeichen oder andere Wörter in anderen Sprachen.
            "\\s+" + // Ein oder mehrere Leerzeichen.
            "(?:\"\"\\s+)?" + // Nicht erfassendes optionales "" und ein oder mehrere Leerzeichen.
            "(\\\\l\\s+)?" + // Optionales \l-Flag, gefolgt von einem oder mehreren Leerzeichen.
            "\"" +     // Ein Apostroph.
            "([^\"]+)" + // Ein oder mehrere Zeichen, ausgenommen Apostroph (Ziel des Hyperlinks).
            "\"" // Ein schließender Apostroph.
        );
    }
}
```

### Siehe auch

* class [FieldChar](../fieldchar/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
