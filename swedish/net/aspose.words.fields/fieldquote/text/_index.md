---
title: FieldQuote.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words för .NET
description: FieldQuote Text-egenskap. Hämta eller ange enkelt text för förbättrad datahantering. Effektivisera ditt arbetsflöde med den här kraftfulla funktionen!
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldquote/text/
---
## FieldQuote.Text property

Hämtar eller ställer in texten som ska hämtas.

```csharp
public string Text { get; set; }
```

## Exempel

Visar att använda CITAT-fältet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett QUOTE-fält, som visar värdet för dess Text-egenskap.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Infoga ett CITAT-fält och kapsla ett DATUM-fält inuti det.
// DATUM-fält uppdaterar sitt värde till dagens datum varje gång vi öppnar dokumentet med Microsoft Word.
// Att kapsla DATUM-fältet inuti CITAT-fältet på detta sätt kommer att frysa dess värde
// till det datum då vi skapade dokumentet.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Uppdatera alla fält för att visa korrekta resultat.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

### Se även

* class [FieldQuote](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
