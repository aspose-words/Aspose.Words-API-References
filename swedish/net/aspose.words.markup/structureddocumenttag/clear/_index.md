---
title: StructuredDocumentTag.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words för .NET
description: Rensa enkelt innehållet i din strukturerade dokumenttagg med metoden Rensa och visa en definierad platshållare för förbättrad dokumenthantering.
type: docs
weight: 360
url: /sv/net/aspose.words.markup/structureddocumenttag/clear/
---
## StructuredDocumentTag.Clear method

Rensar innehållet i den här strukturerade dokumenttaggen och visar en platshållare om den är definierad.

```csharp
public void Clear()
```

## Anmärkningar

Det är inte möjligt att rensa innehållet i en strukturerad dokumenttagg om den har revideringar.

Om den här strukturerade dokumenttaggen mappas till anpassad XML (med hjälp av[`XmlMapping`](../xmlmapping/)(egenskapen ) rensas den refererade XML-noden.

## Exempel

Visar hur man tar bort innehållet i taggelement i strukturerade dokument.

```csharp
Document doc = new Document();

// Skapa en strukturerad dokumenttagg i vanlig text och lägg sedan till den i dokumentet.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Denna strukturerade dokumenttagg, som är i form av en textruta, visar redan platshållartext.
Assert.AreEqual("Click here to enter text.", tag.GetText().Trim());
Assert.True(tag.IsShowingPlaceholderText);

// Skapa en byggsten med textinnehåll.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;
BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "My placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.EnsureMinimum();
substituteBlock.FirstSection.Body.FirstParagraph.AppendChild(new Run(glossaryDoc, "Custom placeholder text."));
glossaryDoc.AppendChild(substituteBlock);

// Ange egenskapen "PlaceholderName" för den strukturerade dokumenttaggen till namnet på vårt byggblock för att få
// taggen för det strukturerade dokumentet för att visa innehållet i byggblocket istället för den ursprungliga standardtexten.
tag.PlaceholderName = "My placeholder";

Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
Assert.True(tag.IsShowingPlaceholderText);

// Redigera texten i den strukturerade dokumenttaggen och dölj platshållartexten.
Run run = (Run)tag.GetChild(NodeType.Run, 0, true);
run.Text = "New text.";
tag.IsShowingPlaceholderText = false;

Assert.AreEqual("New text.", tag.GetText().Trim());

// Använd metoden "Rensa" för att rensa innehållet i den här strukturerade dokumenttaggen och visa platshållaren igen.
tag.Clear();

Assert.True(tag.IsShowingPlaceholderText);
Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
```

### Se även

* class [StructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
