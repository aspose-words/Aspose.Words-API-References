---
title: ListLabel.LabelValue
linktitle: LabelValue
articleTitle: LabelValue
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ListLabel LabelValue för att enkelt hämta numeriska värden för etiketter, vilket förbättrar din datahantering och rapporteringseffektivitet.
type: docs
weight: 30
url: /sv/net/aspose.words.lists/listlabel/labelvalue/
---
## ListLabel.LabelValue property

Hämtar ett numeriskt värde för denna etikett.

```csharp
public int LabelValue { get; }
```

## Anmärkningar

Använd[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) metod för att uppdatera värdet på den här egenskapen.

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

* class [ListLabel](../)
* namnutrymme [Aspose.Words.Lists](../../../aspose.words.lists/)
* hopsättning [Aspose.Words](../../../)
