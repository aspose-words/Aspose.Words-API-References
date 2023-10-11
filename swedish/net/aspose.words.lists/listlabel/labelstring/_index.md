---
title: ListLabel.LabelString
second_title: Aspose.Words för .NET API Referens
description: ListLabel fast egendom. Får en strängrepresentation av listetikett.
type: docs
weight: 20
url: /sv/net/aspose.words.lists/listlabel/labelstring/
---
## ListLabel.LabelString property

Får en strängrepresentation av listetikett.

```csharp
public string LabelString { get; }
```

### Exempel

Visar hur man extraherar listetiketterna för alla stycken som är listobjekt.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// Hitta om vi har styckelistan. I vårt dokument använder vår lista vanliga arabiska siffror,
// som börjar vid tre och slutar vid sex.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Det här är texten vi får när vi matar ut den här noden till textformat.
     // Denna textutgång kommer att utelämna listetiketter. Trimma alla tecken i styckeformatering.
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Detta får styckets position på den aktuella nivån i listan. Om vi har en lista med flera nivåer,
    // detta kommer att berätta vilken position det är på den nivån.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Kombinera dem för att inkludera listetiketten med texten i utdata.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Se även

* class [ListLabel](../)
* namnutrymme [Aspose.Words.Lists](../../listlabel/)
* hopsättning [Aspose.Words](../../../)


