---
title: Run
second_title: Aspose.Words för .NET API Referens
description: Initierar en ny instans av Springa class.
type: docs
weight: 10
url: /sv/net/aspose.words/run/run/
---
## Run(DocumentBase) {#constructor}

Initierar en ny instans av **Springa** class.

```csharp
public Run(DocumentBase doc)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | DocumentBase | Ägardokumentet. |

### Anmärkningar

När **Springa** skapas, det tillhör det angivna dokumentet, men är inte ännu en del av dokumentet och **ParentNode** är inget.

Att lägga till **Springa** till dokumentet använd InsertAfter eller InsertBefore på det stycke där du vill att körningen ska infogas.

### Exempel

Visar hur man konstruerar ett Aspose.Words-dokument för hand.

```csharp
Document doc = new Document();

// Ett tomt dokument innehåller ett avsnitt, en brödtext och ett stycke.
// Anropa metoden "RemoveAllChildren" för att ta bort alla dessa noder,
// och slutar med en dokumentnod utan underordnade.
doc.RemoveAllChildren();

// Det här dokumentet har nu inga sammansatta underordnade noder som vi kan lägga till innehåll till.
// Om vi vill redigera den måste vi fylla på dess nodsamling.
// Skapa först ett nytt avsnitt och lägg sedan till det som ett underordnat dokument i rotdokumentnoden.
Section section = new Section(doc);
doc.AppendChild(section);

// Ställ in några sidinställningar för avsnittet.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// En sektion behöver en kropp som kommer att innehålla och visa allt dess innehåll
// på sidan mellan avsnittets sidhuvud och sidfot.
Body body = new Body(doc);
section.AppendChild(body);

// Skapa ett stycke, ange några formateringsegenskaper och lägg sedan till det som ett underordnat stycke i brödtexten.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Slutligen, lägg till lite innehåll för att göra dokumentet. Skapa en löprunda,
// ställ in dess utseende och innehåll och lägg sedan till det som ett barn till stycket.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Se även

* class [DocumentBase](../../documentbase)
* class [Run](../../run)
* namnutrymme [Aspose.Words](../../run)
* hopsättning [Aspose.Words](../../../)

---

## Run(DocumentBase, string) {#constructor_1}

Initierar en ny instans av **Springa** class.

```csharp
public Run(DocumentBase doc, string text)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | DocumentBase | Ägardokumentet. |
| text | String | Löpningens text. |

### Anmärkningar

När **Springa** skapas, det tillhör det angivna dokumentet, men är inte ännu en del av dokumentet och **ParentNode** är inget.

Att lägga till **Springa** till dokumentet använd InsertAfter eller InsertBefore på det stycke där du vill att körningen ska infogas.

### Exempel

Visar hur man formaterar en serie text med dess teckensnittsegenskap.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

### Se även

* class [DocumentBase](../../documentbase)
* class [Run](../../run)
* namnutrymme [Aspose.Words](../../run)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
