---
title: NodeList Class
linktitle: NodeList
articleTitle: NodeList
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.NodeList, Ihre Lösung für die effiziente Verwaltung von XPath-Abfrageergebnissen und die Verbesserung der Dokumentverarbeitungsfunktionen.
type: docs
weight: 4910
url: /de/net/aspose.words/nodelist/
---
## NodeList class

Stellt eine Sammlung von Knoten dar, die einer XPath-Abfrage entsprechen, die mit dem[`SelectNodes`](../compositenode/selectnodes/) Methode.

Um mehr zu erfahren, besuchen Sie die[Aspose.Words Dokumentobjektmodell (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Dokumentationsartikel.

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
| [GetEnumerator](../../aspose.words/nodelist/getenumerator/)() | Bietet eine einfache Iteration im „foreach“-Stil über die Knotensammlung. |
| [ToArray](../../aspose.words/nodelist/toarray/)() | Kopiert alle Knoten aus der Sammlung in ein neues Knoten-Array. |

## Bemerkungen

`NodeList` wird zurückgegeben von[`SelectNodes`](../compositenode/selectnodes/) und enthält eine Sammlung von Knoten, die der XPath-Abfrage entsprechen.

`NodeList` unterstützt indizierten Zugriff und Iteration.

Behandeln Sie die`NodeList` Sammlung als „Momentaufnahme“-Sammlung.`NodeList` startet als „Live“-Sammlung, da die Knoten beim Ausführen der XPath-Abfrage nicht tatsächlich abgerufen werden. Die Knoten werden nur beim Zugriff abgerufen und zu diesem Zeitpunkt werden der Knoten und alle Knoten, die ihm vorangehen, zwischengespeichert und bilden eine „Snapshot“-Sammlung.

## Beispiele

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

* class [Node](../node/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
