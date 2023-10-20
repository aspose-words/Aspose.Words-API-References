---
title: FieldGoToButton.DisplayText
linktitle: DisplayText
articleTitle: DisplayText
second_title: Aspose.Words för .NET
description: FieldGoToButton DisplayText fast egendom. Hämtar eller ställer in texten för knappen som visas i dokumentet så att den kan väljas för att aktivera hoppet i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldgotobutton/displaytext/
---
## FieldGoToButton.DisplayText property

Hämtar eller ställer in texten för "knappen" som visas i dokumentet, så att den kan väljas för att aktivera hoppet.

```csharp
public string DisplayText { get; set; }
```

## Exempel

Visar för att infoga ett GOTOBUTTON-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Lägg till ett GOTOBUTTON-fält. När vi dubbelklickar på det här fältet i Microsoft Word,
// det tar textmarkören till bokmärket vars namn platsegenskapen refererar till.
FieldGoToButton field = (FieldGoToButton)builder.InsertField(FieldType.FieldGoToButton, true);
field.DisplayText = "My Button";
field.Location = "MyBookmark";

Assert.AreEqual(" GOTOBUTTON  MyBookmark My Button", field.GetFieldCode());

// Infoga ett giltigt bokmärke för fältet att referera till.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark(field.Location);
builder.Writeln("Bookmark text contents.");
builder.EndBookmark(field.Location);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.GOTOBUTTON.docx");
```

### Se även

* class [FieldGoToButton](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
