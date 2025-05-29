---
title: TabStop Class
linktitle: TabStop
articleTitle: TabStop
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.TabStop, din lösning för anpassade tabbstopp i dokumentformatering. Förbättra dina dokument med precision och enkelthet!
type: docs
weight: 7050
url: /sv/net/aspose.words/tabstop/
---
## TabStop class

Representerar ett enda anpassat tabbstopp.`TabStop` objektet är en medlem av the [`TabStopCollection`](../tabstopcollection/) samling.

För att lära dig mer, besök[Aspose.Words-dokumentobjektmodell (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) dokumentationsartikel.

```csharp
public sealed class TabStop
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [TabStop](tabstop/#constructor)(*double*) | Initierar en ny instans av den här klassen. |
| [TabStop](tabstop/#constructor_1)(*double, [TabAlignment](../tabalignment/), [TabLeader](../tableader/)*) | Initierar en ny instans av den här klassen. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Alignment](../../aspose.words/tabstop/alignment/) { get; set; } | Hämtar eller ställer in textjusteringen vid detta tabbstopp. |
| [IsClear](../../aspose.words/tabstop/isclear/) { get; } | Returer`sann` om detta tabbstopp rensar alla befintliga tabbstopp i denna position. |
| [Leader](../../aspose.words/tabstop/leader/) { get; set; } | Hämtar eller anger typen av hänvisningslinjen som visas under tabbtecknet. |
| [Position](../../aspose.words/tabstop/position/) { get; } | Hämtar tabbstoppets position i punkter. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Equals](../../aspose.words/tabstop/equals/#equals)(*TabStop*) | Jämförs med den angivna`TabStop` . |
| override [GetHashCode](../../aspose.words/tabstop/gethashcode/)() | Beräknar hashkod för detta objekt. |

## Anmärkningar

Normalt sett anger ett tabbstopp en position där ett tabbstopp finns. Men eftersom tabbstopp kan ärvas från överordnade stilar kan det behövas att underobjektet explicit definierar att det inte finns något tabbstopp vid en given position. För att rensa ett ärvt tabbstopp vid en given position, skapa ett`TabStop` objekt och set [`Alignment`](./alignment/) tillClear.

För mer information se[`TabStopCollection`](../tabstopcollection/).

## Exempel

Visar hur man ändrar positionen för höger tabbstopp i stycken relaterade till innehållsförteckningen.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// Iterera genom alla stycken med resultatbaserade stilar baserade på innehållsförteckningen; detta är vilken stil som helst mellan innehållsförteckning och innehållsförteckning9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Hämta den första tabbtangenten som används i detta stycke, detta ska vara den tabbtangent som används för att justera sidnumren.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // Ersätt den första standardtabbstoppet med en anpassad tabbstopp.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
