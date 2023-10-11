---
title: Class NodeList
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.NodeList klas. Stellt eine Sammlung von Knoten dar die einer XPathAbfrage entsprechen die mit ausgeführt wurdeSelectNodes method.
type: docs
weight: 4220
url: /de/net/aspose.words/nodelist/
---
## NodeList class

Stellt eine Sammlung von Knoten dar, die einer XPath-Abfrage entsprechen, die mit ausgeführt wurde[`SelectNodes`](../compositenode/selectnodes/) method.

Um mehr zu erfahren, besuchen Sie die[Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Dokumentationsartikel.

```csharp
public class NodeList : IEnumerable<Node>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/nodelist/count/) { get; } | Ruft die Anzahl der Knoten in der Liste ab. |
| [Item](../../aspose.words/nodelist/item/) { get; } | Ruft einen Knoten am angegebenen Index ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetEnumerator](../../aspose.words/nodelist/getenumerator/)() | Bietet eine einfache Iteration im „foreach“-Stil über die Sammlung von Knoten. |
| [ToArray](../../aspose.words/nodelist/toarray/)() | Kopiert alle Knoten aus der Sammlung in ein neues Array von Knoten. |

### Bemerkungen

`NodeList` wird zurückgegeben von[`SelectNodes`](../compositenode/selectnodes/) und enthält eine Sammlung von Knoten, die der XPath-Abfrage entsprechen.

`NodeList` unterstützt indizierten Zugriff und Iteration.

Behandeln Sie die`NodeList` Sammlung als „Snapshot“-Sammlung.`NodeList`startet als „Live“-Sammlung, da die Knoten nicht tatsächlich abgerufen werden, wenn die XPath-Abfrage ausgeführt wird. Die Knoten werden nur beim Zugriff abgerufen und zu diesem Zeitpunkt werden der Knoten und alle ihm vorausgehenden Knoten zwischengespeichert und bilden eine „Snapshot“-Sammlung.

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

            // Hyperlinks in einem Word-Dokument sind Felder. Um mit der Suche nach Hyperlinks zu beginnen, müssen wir zunächst alle Felder finden.
            // Verwenden Sie die Methode „SelectNodes“, um alle Felder im Dokument über einen XPath zu finden.
            NodeList fieldStarts = doc.SelectNodes("//FieldStart");

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

     ///<summary>
      ///HYPERLINK-Felder enthalten Hyperlinks im Dokumentkörper und zeigen diese an. Ein Feld in Aspose.Words
      ///besteht aus mehreren Knoten, und es könnte schwierig sein, mit allen diesen Knoten direkt zu arbeiten.
     ///Diese Implementierung funktioniert nur, wenn der Hyperlink-Code und der Name jeweils nur aus einem Run-Knoten bestehen.
    ///
     ///Die Knotenstruktur für Felder ist wie folgt:
     ///
     ///[FieldStart][Run - field code][FieldSeparator][Run - field result][FieldEnd]
     ///
     ///Below are two example field codes of HYPERLINK fields:
     ///HYPERLINK "url"
     ///HYPERLINK \l "bookmark name"
     ///
     ///A field's "Result" property contains text that the field displays in the document body to the user.
     ///</summary>
    internal class Hyperlink
    {
        internal Hyperlink(FieldStart fieldStart)
        {
            if (fieldStart == null)
                throw new ArgumentNullException("fieldStart");
            if (fieldStart.FieldType != FieldType.FieldHyperlink)
                throw new ArgumentException("Field start type must be FieldHyperlink.");

            mFieldStart = fieldStart;

            // Den Feldtrennknoten finden.
            mFieldSeparator = FindNextSibling(mFieldStart, NodeType.FieldSeparator);
            if (mFieldSeparator == null)
                throw new InvalidOperationException("Cannot find field separator.");

             // Normalerweise können wir immer den Endknoten des Feldes finden, aber das Beispieldokument
             // enthält einen Absatzumbruch innerhalb eines Hyperlinks, der das Feldende setzt
            // im nächsten Absatz. Es wird viel komplizierter sein, Felder zu verwalten, die sich über mehrere Felder erstrecken
            // Absätze richtig. In diesem Fall reicht es aus, das Feldende auf Null zu setzen.
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

            // Der Feldcode sieht etwa wie „HYPERLINK „http:\\www.myurl.com““ aus, kann aber aus mehreren Durchläufen bestehen.
            string fieldCode = GetTextSameParent(mFieldStart.NextSibling, mFieldSeparator);
            Match match = gRegex.Match(fieldCode.Trim());

            // Der Hyperlink ist lokal, wenn \l im Feldcode vorhanden ist.
            mIsLocal = match.Groups[1].Length > 0; 
            mTarget = match.Groups[2].Value;
        }

         ///<summary>
         ///Gets or sets the display name of the hyperlink.
         ///</summary>
        internal string Name
        {
            get => GetTextSameParent(mFieldSeparator, mFieldEnd); 
            set
            {
                 // Der Anzeigename des Hyperlinks wird im Feldergebnis gespeichert, bei dem es sich um eine Ausführung handelt
                // Knoten zwischen Feldtrenner und Feldende.
                Run fieldResult = (Run) mFieldSeparator.NextSibling;
                fieldResult.Text = value;

                // Wenn das Feldergebnis aus mehr als einem Lauf besteht, löschen Sie diese Läufe.
                RemoveSameParent(fieldResult.NextSibling, mFieldEnd);
            }
        }

         ///<summary>
         ///Gets or sets the target URL or bookmark name of the hyperlink.
         ///</summary>
        internal string Target
        {
            get => mTarget;
            set
            {
                mTarget = value;
                UpdateFieldCode();
            }
        }

         ///<summary>
         ///True if the hyperlinks target is a bookmark inside the document. False if the hyperlink is a URL.
         ///</summary>
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
            // Der Feldcode eines Feldes befindet sich in einem Run-Knoten zwischen dem Startknoten des Feldes und dem Feldtrennzeichen.
            Run fieldCode = (Run) mFieldStart.NextSibling;
            fieldCode.Text = string.Format("HYPERLINK {0}\"{1}\"", ((mIsLocal) ? "\\l " : ""), mTarget);

            // Wenn der Feldcode aus mehr als einem Lauf besteht, löschen Sie diese Läufe.
            RemoveSameParent(fieldCode.NextSibling, mFieldSeparator);
        }

         ///<summary>
         ///Goes through siblings starting from the start node until it finds a node of the specified type or null.
         ///</summary>
        private static Node FindNextSibling(Node startNode, NodeType nodeType)
        {
            for (Node node = startNode; node != null; node = node.NextSibling)
            {
                if (node.NodeType == nodeType)
                    return node;
            }

            return null;
        }

         ///<summary>
         ///Retrieves text from start up to but not including the end node.
         ///</summary>
        private static string GetTextSameParent(Node startNode, Node endNode)
        {
            if ((endNode != null) && (startNode.ParentNode != endNode.ParentNode))
                throw new ArgumentException("Start and end nodes are expected to have the same parent.");

            StringBuilder builder = new StringBuilder();
            for (Node child = startNode; !child.Equals(endNode); child = child.NextSibling)
                builder.Append(child.GetText());

            return builder.ToString();
        }

         ///<summary>
         ///Removes nodes from start up to but not including the end node.
         ///Assumes that the start and end nodes have the same parent.
         ///</summary>
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
            "\\S+" + // Ein oder mehrere HYPERLINK-Zeichen, die keine Leerzeichen sind, oder ein anderes Wort in anderen Sprachen.
            "\\s+" + // Ein oder mehrere Leerzeichen.
            "(?:\"\"\\s+)?" + // Nicht erfassendes optionales „“ und ein oder mehrere Leerzeichen.
            "(\\\\l\\s+)?" + // Optionales \l-Flag, gefolgt von einem oder mehreren Leerzeichen.
            "\"" +  // Ein Apostroph.
            "([^\"]+)" + // Ein oder mehrere Zeichen, außer dem Apostroph (Hyperlink-Ziel).
            "\"" // Ein abschließendes Apostroph.
        );
    }
}
```

### Siehe auch

* class [Node](../node/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


