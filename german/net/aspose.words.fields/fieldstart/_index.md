---
title: FieldStart
second_title: Aspose.Words für .NET-API-Referenz
description: Repräsentiert den Anfang eines WordFeldes in einem Dokument.
type: docs
weight: 2280
url: /de/net/aspose.words.fields/fieldstart/
---
## FieldStart class

Repräsentiert den Anfang eines Word-Feldes in einem Dokument.

```csharp
public class FieldStart : FieldChar
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [FieldData](../../aspose.words.fields/fieldstart/fielddata/) { get; } | Ruft benutzerdefinierte Felddaten ab, die dem Feld zugeordnet sind. |
| [FieldType](../../aspose.words.fields/fieldchar/fieldtype/) { get; } | Gibt den Feldtyp zurück. |
| [Font](../../aspose.words/inline/font/) { get; } | Bietet Zugriff auf die Schriftformatierung dieses Objekts. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Gibt wahr zurück, wenn dieser Knoten andere Knoten enthalten kann. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsnachverfolgung aktiviert war. |
| [IsDirty](../../aspose.words.fields/fieldchar/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Gibt „true“ zurück, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Änderungsverfolgung aktiviert war. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [IsLocked](../../aspose.words.fields/fieldchar/islocked/) { get; set; } | Ruft ab oder legt fest, ob das übergeordnete Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | gibt zurück **Stimmt** wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsnachverfolgung aktiviert war. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | gibt zurück **Stimmt** wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsnachverfolgung aktiviert war. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words.fields/fieldstart/nodetype/) { get; } | gibt zurückFieldStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Ruft das übergeordnete Element ab[`Paragraph`](../../aspose.words/paragraph/) dieses Knotens. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten unmittelbar vor diesem Knoten ab. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt a zurück **Bereich** Objekt, das den Teil eines Dokuments darstellt, das in diesem Knoten enthalten ist. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words.fields/fieldstart/accept/)(DocumentVisitor) | Akzeptiert einen Besucher. |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Ruft den ersten Vorfahren der angegebenen ab[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| [GetField](../../aspose.words.fields/fieldchar/getfield/)() | Gibt ein Feld für das Feld char. zurück |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Ruft das Sonderzeichen ab, das dieser Knoten darstellt. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ruft den nächsten Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ruft den vorherigen Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in einen String. |

### Bemerkungen

`FieldStart` ist ein Knoten auf Inline-Ebene und wird durch the dargestellt.[`FieldStartChar`](../../aspose.words/controlchar/fieldstartchar/) Steuerzeichen im Dokument.

`FieldStart` kann nur ein Kind von sein[`Paragraph`](../../aspose.words/paragraph/).

Ein vollständiges Feld in einem Microsoft Word-Dokument ist eine komplexe Struktur, die aus einem Feldanfangszeichen, einem Feldcode, einem Feldtrennzeichen, einem Feldergebnis und einem Feldendezeichen besteht. Einige Felder haben nur Feldanfang, Feldcode und Feldende.

Verwenden Sie zum einfachen Einfügen eines neuen Felds in ein Dokument die[`InsertField`](../../aspose.words/documentbuilder/insertfield/) Methode.

### Beispiele

Zeigt, wie mit einer Sammlung von Feldern gearbeitet wird.

```csharp
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

    // Über die Feldsammlung iterieren und Inhalt und Typ ausgeben
    // jedes Feldes mit einer benutzerdefinierten Besucherimplementierung.
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

/// <summary>
/// Besucherimplementierung dokumentieren, die Feldinformationen druckt.
/// </summary>
public class FieldVisitor : DocumentVisitor
{
    public FieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Ruft den Klartext des Dokuments ab, das vom Besucher angesammelt wurde.
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

Zeigt, wie Sie alle Hyperlinks in einem Word-Dokument finden und dann ihre URLs und Anzeigenamen ändern.

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

            // Hyperlinks in einem Word-Dokument sind Felder. Um mit der Suche nach Hyperlinks zu beginnen, müssen wir zuerst alle Felder finden.
            // Verwenden Sie die "SelectNodes"-Methode, um alle Felder im Dokument über einen XPath zu finden.
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

    /// <summary>
    /// HYPERLINK-Felder enthalten und zeigen Hyperlinks im Dokumentkörper an. Ein Feld in Aspose.Words 
    /// besteht aus mehreren Knoten, und es kann schwierig sein, direkt mit all diesen Knoten zu arbeiten. 
    /// Diese Implementierung funktioniert nur, wenn der Hyperlink-Code und -Name jeweils nur aus einem Run-Knoten bestehen.
    ///
    /// Die Knotenstruktur für Felder ist wie folgt:
    /// 
    /// [FieldStart][Run - Feldcode][FieldSeparator][Run - Feldergebnis][FieldEnd]
    /// 
    /// Unten sind zwei Beispiel-Feldcodes von HYPERLINK-Feldern:
    /// HYPERLINK "url"
    /// HYPERLINK \l "Name des Lesezeichens"
    /// 
    /// Die Eigenschaft "Ergebnis" eines Felds enthält Text, den das Feld dem Benutzer im Hauptteil des Dokuments anzeigt.
    /// </summary>
    internal class Hyperlink
    {
        internal Hyperlink(FieldStart fieldStart)
        {
            if (fieldStart == null)
                throw new ArgumentNullException("fieldStart");
            if (fieldStart.FieldType != FieldType.FieldHyperlink)
                throw new ArgumentException("Field start type must be FieldHyperlink.");

            mFieldStart = fieldStart;

            // Suchen Sie den Feldtrenner-Knoten.
            mFieldSeparator = FindNextSibling(mFieldStart, NodeType.FieldSeparator);
            if (mFieldSeparator == null)
                throw new InvalidOperationException("Cannot find field separator.");

            // Normalerweise finden wir immer den Endknoten des Feldes, aber das Beispieldokument 
            // enthält einen Absatzumbruch innerhalb eines Hyperlinks, wodurch das Feld endet 
            // im nächsten Absatz. Wesentlich komplizierter wird es, Felder zu handhaben, die sich über mehrere Felder erstrecken 
            // Absätze korrekt. In diesem Fall reicht es aus, das Feldende auf null zu setzen.
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

            // Feldcode sieht etwa so aus wie "HYPERLINK "http:\\www.myurl.com"", kann aber aus mehreren Läufen bestehen.
            string fieldCode = GetTextSameParent(mFieldStart.NextSibling, mFieldSeparator);
            Match match = gRegex.Match(fieldCode.Trim());

            // Der Hyperlink ist lokal, wenn \l im Feldcode vorhanden ist.
            mIsLocal = match.Groups[1].Length > 0; 
            mTarget = match.Groups[2].Value;
        }

        /// <summary>
        /// Ruft den Anzeigenamen des Hyperlinks ab oder legt ihn fest.
        /// </summary>
        internal string Name
        {
            get => GetTextSameParent(mFieldSeparator, mFieldEnd); 
            set
            {
                // Anzeigename des Hyperlinks wird im Feld result gespeichert, das ein Run ist 
                // Knoten zwischen Feldtrenner und Feldende.
                Run fieldResult = (Run) mFieldSeparator.NextSibling;
                fieldResult.Text = value;

                // Wenn das Feldergebnis aus mehr als einem Lauf besteht, diese Läufe löschen.
                RemoveSameParent(fieldResult.NextSibling, mFieldEnd);
            }
        }

        /// <summary>
        /// Ruft die Ziel-URL oder den Lesezeichennamen des Hyperlinks ab oder legt sie fest.
        /// </summary>
        internal string Target
        {
            get => mTarget;
            set
            {
                mTarget = value;
                UpdateFieldCode();
            }
        }

        /// <summary>
        /// Wahr, wenn das Ziel des Hyperlinks ein Lesezeichen im Dokument ist. False, wenn der Hyperlink eine URL ist.
        /// </summary>
        internal bool IsLocal
        {
            get => mIsLocal; 
            set
            {
                mIsLocal = value;
                UpdateFieldCode();
            }
        }

        private void UpdateFieldCode()
        {
            // Der Feldcode eines Felds befindet sich in einem Run-Knoten zwischen dem Startknoten des Felds und dem Feldtrennzeichen.
            Run fieldCode = (Run) mFieldStart.NextSibling;
            fieldCode.Text = string.Format("HYPERLINK {0}\"{1}\"", ((mIsLocal) ? "\\l " : ""), mTarget);

            // Wenn der Feldcode aus mehr als einem Lauf besteht, diese Läufe löschen.
            RemoveSameParent(fieldCode.NextSibling, mFieldSeparator);
        }

        /// <summary>
        /// Geht vom Startknoten ausgehend durch Geschwister, bis ein Knoten des angegebenen Typs oder null gefunden wird.
        /// </summary>
        private static Node FindNextSibling(Node startNode, NodeType nodeType)
        {
            for (Node node = startNode; node != null; node = node.NextSibling)
            {
                if (node.NodeType == nodeType)
                    return node;
            }

            return null;
        }

        /// <summary>
        /// Ruft Text vom Anfang bis zum Endknoten ab, schließt diesen jedoch nicht ein.
        /// </summary>
        private static string GetTextSameParent(Node startNode, Node endNode)
        {
            if ((endNode != null) && (startNode.ParentNode != endNode.ParentNode))
                throw new ArgumentException("Start and end nodes are expected to have the same parent.");

            StringBuilder builder = new StringBuilder();
            for (Node child = startNode; !child.Equals(endNode); child = child.NextSibling)
                builder.Append(child.GetText());

            return builder.ToString();
        }

        /// <summary>
        /// Entfernt Knoten vom Anfang bis zum Endknoten, jedoch nicht darunter.
        /// Geht davon aus, dass Start- und Endknoten denselben Elternknoten haben.
        /// </summary>
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
            "\\S+" + // Ein oder mehrere Nicht-Leerzeichen HYPERLINK oder ein anderes Wort in anderen Sprachen.
            "\\s+" + // Ein oder mehrere Leerzeichen.
            "(?:\"\"\\s+)?" + // Nicht erfassendes optionales "" und ein oder mehrere Leerzeichen.
            "(\\\\l\\s+)?" + // Optionales Flag \l gefolgt von einem oder mehreren Leerzeichen.
            "\"" + // Ein Apostroph.    
            "([^\"]+)" + // Ein oder mehrere Zeichen, mit Ausnahme des Apostrophs (Ziel des Hyperlinks).
            "\"" // Ein schließender Apostroph.
        );
    }
}
```

### Siehe auch

* class [FieldChar](../fieldchar/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
