---
title: NodeList
second_title: Aspose.Words für .NET-API-Referenz
description: Stellt eine Sammlung von Knoten dar die mit einer XPath-Abfrage übereinstimmen die mit ausgeführt wurdeSelectNodes./compositenode/selectnodes Methode.
type: docs
weight: 3980
url: /de/net/aspose.words/nodelist/
---
## NodeList class

Stellt eine Sammlung von Knoten dar, die mit einer XPath-Abfrage übereinstimmen, die mit ausgeführt wurde[`SelectNodes`](../compositenode/selectnodes) Methode.

```csharp
public class NodeList : IEnumerable<Node>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/nodelist/count) { get; } | Ruft die Anzahl der Knoten in der Liste ab. |
| [Item](../../aspose.words/nodelist/item) { get; } | Ruft einen Knoten am angegebenen Index ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetEnumerator](../../aspose.words/nodelist/getenumerator)() | Bietet eine einfache Iteration im "foreach"-Stil über die Sammlung von Knoten. |
| [ToArray](../../aspose.words/nodelist/toarray)() | Kopiert alle Knoten aus der Sammlung in ein neues Array von Knoten. |

### Bemerkungen

**Knotenliste** wird von zurückgegeben[`SelectNodes`](../compositenode/selectnodes) und enthält eine Sammlung von Knoten, die mit der XPath-Abfrage übereinstimmen.

**Knotenliste** unterstützt indizierten Zugriff und Iteration.

Behandle die **Knotenliste** Sammlung als "Schnappschuss"-Sammlung. **Knotenliste**startet als eine „Live“-Sammlung, da die Knoten nicht tatsächlich abgerufen werden, wenn die XPath-Abfrage ausgeführt wird. Die Knoten werden nur beim Zugriff abgerufen, und zu diesem Zeitpunkt werden der Knoten und alle ihm vorausgehenden Knoten zwischengespeichert und bilden eine „Snapshot“-Sammlung.

### Beispiele

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

* class [Node](../node)
* namensraum [Aspose.Words](../../aspose.words)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
