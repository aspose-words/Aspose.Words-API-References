---
title: Run
linktitle: Run
articleTitle: Run
second_title: Aspose.Words för .NET
description: Skapa och anpassa din Run-klassinstans utan ansträngning. Lås upp kraftfulla funktioner för effektiv prestanda och förbättrad funktionalitet.
type: docs
weight: 10
url: /sv/net/aspose.words/run/run/
---
## Run(*[DocumentBase](../../documentbase/)*) {#constructor}

Initierar en ny instans av[`Run`](../) klass.

```csharp
public Run(DocumentBase doc)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | DocumentBase | Ägardokumentet. |

## Anmärkningar

När[`Run`](../) skapas, tillhör den det angivna dokumentet, men är ännu inte en del av dokumentet och[`ParentNode`](../../node/parentnode/) är`null`.

Att lägga till[`Run`](../) till dokumentanvändningen[`InsertAfter`](../../compositenode/insertafter/) eller[`InsertBefore`](../../compositenode/insertbefore/) på stycket där du vill infoga löpsekvensen.

## Exempel

Visar hur man konstruerar ett Aspose.Words-dokument för hand.

```csharp
Document doc = new Document();

// Ett tomt dokument innehåller ett avsnitt, en brödtext och ett stycke.
// Anropa metoden "RemoveAllChildren" för att ta bort alla dessa noder,
// och slutar med en dokumentnod utan barn.
doc.RemoveAllChildren();

// Det här dokumentet har nu inga sammansatta undernoder som vi kan lägga till innehåll till.
// Om vi vill redigera den måste vi fylla i dess nodsamling igen.
// Skapa först en ny sektion och lägg sedan till den som ett underordnat avsnitt till rotdokumentnoden.
Section section = new Section(doc);
doc.AppendChild(section);

// Ange vissa sidinställningar för avsnittet.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// En sektion behöver en brödtext, som innehåller och visar allt dess innehåll
// på sidan mellan avsnittets sidhuvud och sidfot.
Body body = new Body(doc);
section.AppendChild(body);

// Skapa ett stycke, ange några formateringsegenskaper och lägg sedan till det som ett underordnat stycke i brödtexten.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Slutligen, lägg till lite innehåll för att göra dokumentet. Skapa en körning,
// ange dess utseende och innehåll och lägg sedan till det som ett underordnat stycke.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Se även

* class [DocumentBase](../../documentbase/)
* class [Run](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## Run(*[DocumentBase](../../documentbase/), string*) {#constructor_1}

Initierar en ny instans av**Sikt** klass.

```csharp
public Run(DocumentBase doc, string text)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | DocumentBase | Ägardokumentet. |
| text | String | Löpningens text. |

## Anmärkningar

När[`Run`](../) skapas, tillhör den det angivna dokumentet, men är ännu inte en del av dokumentet och[`ParentNode`](../../node/parentnode/) är`null`.

Att lägga till[`Run`](../) till dokumentanvändningen[`InsertAfter`](../../compositenode/insertafter/) eller[`InsertBefore`](../../compositenode/insertbefore/) på stycket där du vill infoga löpsekvensen.

## Exempel

Visar hur man formaterar en textsekvens med hjälp av dess font-egenskap.

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

* class [DocumentBase](../../documentbase/)
* class [Run](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
