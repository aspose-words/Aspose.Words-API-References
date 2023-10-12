---
title: Paragraph.GetText
second_title: Aspose.Words för .NET API Referens
description: Paragraph metod. Hämtar texten i detta stycke inklusive slutet av styckets tecken.
type: docs
weight: 280
url: /sv/net/aspose.words/paragraph/gettext/
---
## Paragraph.GetText method

Hämtar texten i detta stycke inklusive slutet av styckets tecken.

```csharp
public override string GetText()
```

### Anmärkningar

Texten för alla underordnade noder är sammanlänkade och slutet av styckets tecken läggs till enligt följande:

* Om stycket är det sista stycket i[`Body`](../../body/) , sedan [`SectionBreak`](../../controlchar/sectionbreak/) (\x000c) läggs till.
* Om stycket är det sista stycket i[`Cell`](../../../aspose.words.tables/cell/) , sedan [`Cell`](../../controlchar/cell/) (\x0007) läggs till.
* För alla andra paragrafer [`ParagraphBreak`](../../controlchar/paragraphbreak/) (\r) läggs till.

Den returnerade strängen innehåller alla kontroll- och specialtecken som beskrivs i[`ControlChar`](../../controlchar/).

### Exempel

Visar hur man lägger till, uppdaterar och tar bort underordnade noder i en CompositeNodes samling av barn.

```csharp
Document doc = new Document();

// Ett tomt dokument har som standard ett stycke.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Sammansatta noder som vårt stycke kan innehålla andra sammansatta och infogade noder som underordnade.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Skapa ytterligare tre körnoder.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Dokumentets brödtext kommer inte att visa dessa körningar förrän vi infogar dem i en sammansatt nod
// som i sig är en del av dokumentets nodträd, som vi gjorde med den första körningen.
// Vi kan bestämma var textinnehållet i noder som vi infogar
// visas i dokumentet genom att ange en infogningsplats i förhållande till en annan nod i stycket.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Infoga den andra körningen i stycket framför den första körningen.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Infoga den tredje körningen efter den första körningen.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Infoga den första körningen till början av styckets samling av underordnade noder.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Vi kan ändra innehållet i körningen genom att redigera och ta bort befintliga underordnade noder.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Se även

* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../paragraph/)
* hopsättning [Aspose.Words](../../../)


