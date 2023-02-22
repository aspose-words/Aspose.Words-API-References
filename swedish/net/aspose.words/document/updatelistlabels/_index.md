---
title: Document.UpdateListLabels
second_title: Aspose.Words för .NET API Referens
description: Document metod. Uppdaterar listetiketter för alla listobjekt i dokumentet.
type: docs
weight: 740
url: /sv/net/aspose.words/document/updatelistlabels/
---
## Document.UpdateListLabels method

Uppdaterar listetiketter för alla listobjekt i dokumentet.

```csharp
public void UpdateListLabels()
```

### Anmärkningar

Denna metod uppdaterar listetikettegenskaper som t.ex[`LabelValue`](../../../aspose.words.lists/listlabel/labelvalue/) och [`LabelString`](../../../aspose.words.lists/listlabel/labelstring/)för varje[`ListLabel`](../../paragraph/listlabel/) objekt i dokumentet.

Även denna metod kallas ibland implicit när fält i dokumentet uppdateras. Detta är required eftersom vissa fält som kan referera till listnummer (som TOC eller REF) behöver dem vara uppdaterade.

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

* class [Document](../)
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)


