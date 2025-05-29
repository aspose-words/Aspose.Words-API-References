---
title: ListLabel Class
linktitle: ListLabel
articleTitle: ListLabel
second_title: Aspose.Words för .NET
description: Utforska klassen Aspose.Words.Lists.ListLabel för att förbättra din dokumentformatering med anpassningsbara listetikettegenskaper för bättre kontroll och presentation.
type: docs
weight: 3940
url: /sv/net/aspose.words.lists/listlabel/
---
## ListLabel class

Definierar egenskaper som är specifika för en listetikett.

För att lära dig mer, besök[Arbeta med listor](https://docs.aspose.com/words/net/working-with-lists/) dokumentationsartikel.

```csharp
public class ListLabel
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Font](../../aspose.words.lists/listlabel/font/) { get; } | Hämtar teckensnittet för listetiketten. |
| [LabelString](../../aspose.words.lists/listlabel/labelstring/) { get; } | Hämtar en strängrepresentation av listetiketten. |
| [LabelValue](../../aspose.words.lists/listlabel/labelvalue/) { get; } | Hämtar ett numeriskt värde för denna etikett. |

## Exempel

Visar hur man extraherar listetiketterna för alla stycken som är listobjekt.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// Se om vi har styckelistan. I vårt dokument använder vår lista vanliga arabiska siffror,
// som börjar vid tre och slutar vid sex.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Detta är texten vi får när vi skriver ut noden i textformat.
     // Denna textutdata kommer att utelämna listetiketter. Beskär alla tecken för styckeformatering.
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Detta hämtar styckets position på listans aktuella nivå. Om vi har en lista med flera nivåer,
    // detta kommer att berätta för oss vilken position den är på den nivån.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Kombinera dem för att inkludera listetiketten med texten i utdata.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Se även

* namnutrymme [Aspose.Words.Lists](../../aspose.words.lists/)
* hopsättning [Aspose.Words](../../)
