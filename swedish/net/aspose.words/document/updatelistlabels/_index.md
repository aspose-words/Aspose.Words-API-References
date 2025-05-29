---
title: Document.UpdateListLabels
linktitle: UpdateListLabels
articleTitle: UpdateListLabels
second_title: Aspose.Words för .NET
description: Uppdatera enkelt alla listobjektsetiketter i ditt dokument med metoden UpdateListLabels, vilket säkerställer konsekvens och tydlighet i ditt innehåll.
type: docs
weight: 820
url: /sv/net/aspose.words/document/updatelistlabels/
---
## Document.UpdateListLabels method

Uppdaterar listetiketter för alla listobjekt i dokumentet.

```csharp
public void UpdateListLabels()
```

## Anmärkningar

Den här metoden uppdaterar listetikettegenskaper som till exempel[`LabelValue`](../../../aspose.words.lists/listlabel/labelvalue/) och [`LabelString`](../../../aspose.words.lists/listlabel/labelstring/) för varje[`ListLabel`](../../paragraph/listlabel/) objektet i dokumentet.

Dessutom anropas ibland den här metoden implicit när fält i dokumentet uppdateras. Detta är required eftersom vissa fält som kan referera till listnummer (som TOC eller REF) behöver vara uppdaterade.

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

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
