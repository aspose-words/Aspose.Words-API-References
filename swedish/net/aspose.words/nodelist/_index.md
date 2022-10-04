---
title: NodeList
second_title: Aspose.Words för .NET API Referens
description: Representerar en samling noder som matchar en XPathfråga som körs medSelectNodes./compositenode/selectnodes/ metod.
type: docs
weight: 3980
url: /sv/net/aspose.words/nodelist/
---
## NodeList class

Representerar en samling noder som matchar en XPath-fråga som körs med[`SelectNodes`](../compositenode/selectnodes/) metod.

```csharp
public class NodeList : IEnumerable<Node>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words/nodelist/count/) { get; } | Hämtar antalet noder i listan. |
| [Item](../../aspose.words/nodelist/item/) { get; } | Hämtar en nod vid det givna indexet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetEnumerator](../../aspose.words/nodelist/getenumerator/)() | Ger en enkel "foreach" stil iteration över samlingen av noder. |
| [ToArray](../../aspose.words/nodelist/toarray/)() | Kopierar alla noder från samlingen till en ny array av noder. |

### Anmärkningar

**NodeList** returneras av[`SelectNodes`](../compositenode/selectnodes/) och innehåller en samling av noder som matchar XPath-frågan.

**NodeList** stöder indexerad åtkomst och iteration.

Behandla **NodeList** samling som en "snapshot"-samling. **NodeList**starts som en "live"-samling eftersom noderna faktiskt inte hämtas när XPath-frågan körs. Noderna hämtas endast vid åtkomst och vid denna tidpunkt cachelagras noden och alla noder som föregår den och bildar en "snapshot"-samling.

### Exempel

Visar hur du hittar alla hyperlänkar i ett Word-dokument och sedan ändrar deras webbadresser och visningsnamn.

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

            // Hyperlänkar i ett Word-dokument är fält. För att börja leta efter hyperlänkar måste vi först hitta alla fält.
            // Använd metoden "SelectNodes" för att hitta alla fält i dokumentet via en XPath.
            NodeList fieldStarts = doc.SelectNodes("//FieldStart");

            foreach (FieldStart fieldStart in fieldStarts.OfType<FieldStart>())
            {
                if (fieldStart.FieldType == FieldType.FieldHyperlink)
                {
                    Hyperlink hyperlink = new Hyperlink(fieldStart);

                    // Hyperlänkar som länkar till bokmärken har inga webbadresser.
                    if (hyperlink.IsLocal)
                        continue;

                    // Ge varje URL-hyperlänk en ny URL och ett nytt namn.
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
    /// HYPERLINK-fält innehåller och visar hyperlänkar i dokumentets brödtext. Ett fält i Aspose.Words 
    /// består av flera noder, och det kan vara svårt att arbeta med alla dessa noder direkt. 
    /// Den här implementeringen fungerar endast om hyperlänkskoden och namnet består av endast en körnod.
    ///
    /// Nodstrukturen för fält är som följer:
    /// 
    /// [FieldStart][Kör - fältkod][Fältseparator][Kör - fältresultat][FieldEnd]
    /// 
    /// Nedan finns två exempel på fältkoder för HYPERLINK-fält:
    /// HYPERLÄNK "url"
    /// HYPERLÄNK \l "bokmärkesnamn"
    /// 
    /// Ett fälts "Result"-egenskap innehåller text som fältet visar i dokumentets brödtext för användaren.
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

            // Hitta fältseparatornoden.
            mFieldSeparator = FindNextSibling(mFieldStart, NodeType.FieldSeparator);
            if (mFieldSeparator == null)
                throw new InvalidOperationException("Cannot find field separator.");

            // Normalt kan vi alltid hitta fältets slutnod, men exempeldokumentet 
            // innehåller en styckebrytning inuti en hyperlänk, vilket gör att fältet slutar 
            // i nästa stycke. Det blir mycket mer komplicerat att hantera fält som spänner över flera 
            // stycken korrekt. I det här fallet räcker det att tillåta fältänden att vara null.
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

            // Fältkoden ser ut ungefär som "HYPERLINK "http:\\www.myurl.com"", men den kan bestå av flera körningar.
            string fieldCode = GetTextSameParent(mFieldStart.NextSibling, mFieldSeparator);
            Match match = gRegex.Match(fieldCode.Trim());

            // Hyperlänken är lokal om \l finns i fältkoden.
            mIsLocal = match.Groups[1].Length > 0; 
            mTarget = match.Groups[2].Value;
        }

        /// <summary>
        /// Hämtar eller ställer in visningsnamnet för hyperlänken.
        /// </summary>
        internal string Name
        {
            get => GetTextSameParent(mFieldSeparator, mFieldEnd); 
            set
            {
                // Hyperlänkens visningsnamn lagras i fältresultatet, vilket är en körning 
                // nod mellan fältavgränsare och fältslut.
                Run fieldResult = (Run) mFieldSeparator.NextSibling;
                fieldResult.Text = value;

                // Om fältresultatet består av mer än en körning, ta bort dessa körningar.
                RemoveSameParent(fieldResult.NextSibling, mFieldEnd);
            }
        }

        /// <summary>
        /// Hämtar eller ställer in måladressen eller bokmärkesnamnet för hyperlänken.
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
        /// Sant om hyperlänksmålet är ett bokmärke inuti dokumentet. Falskt om hyperlänken är en URL.
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
            // Ett fälts fältkod finns i en Run-nod mellan fältets startnod och fältavgränsare.
            Run fieldCode = (Run) mFieldStart.NextSibling;
            fieldCode.Text = string.Format("HYPERLINK {0}\"{1}\"", ((mIsLocal) ? "\\l " : ""), mTarget);

            // Om fältkoden består av mer än en körning, ta bort dessa körningar.
            RemoveSameParent(fieldCode.NextSibling, mFieldSeparator);
        }

        /// <summary>
        /// Går igenom syskon med start från startnoden tills den hittar en nod av angiven typ eller noll.
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
        /// Hämtar text från start upp till men inte inklusive slutnoden.
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
        /// Tar bort noder från start till men inte inklusive slutnoden.
        /// Antar att start- och slutnoderna har samma förälder.
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
            "\\S+" + // Ett eller flera icke-mellanslag HYPERLINK eller annat ord på andra språk.
            "\\s+" + // Ett eller flera mellanslag.
            "(?:\"\"\\s+)?" + // Icke-fångande valfritt "" och ett eller flera mellanslag.
            "(\\\\l\\s+)?" + // Valfri \l flagga följt av ett eller flera mellanslag.
            "\"" + // En apostrof.    
            "([^\"]+)" + // Ett eller flera tecken, exklusive apostrof (hyperlänksmål).
            "\"" // En avslutande apostrof.
        );
    }
}
```

### Se även

* class [Node](../node/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
