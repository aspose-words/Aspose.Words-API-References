---
title: FieldQuote.Text
second_title: Aspose.Words för .NET API Referens
description: FieldQuote fast egendom. Hämtar eller ställer in texten som ska hämtas.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldquote/text/
---
## FieldQuote.Text property

Hämtar eller ställer in texten som ska hämtas.

```csharp
public string Text { get; set; }
```

### Exempel

Visar att använda fältet CITAT.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett CITAT-fält som visar värdet på dess Text-egenskap.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Infoga ett CITAT-fält och kapsla ett DATUM-fält inuti det.
// DATE-fält uppdaterar sitt värde till det aktuella datumet varje gång vi öppnar dokumentet med Microsoft Word.
// Om du kapar DATUM-fältet inuti CITAT-fältet så här fryser dess värde
// till datumet då vi skapade dokumentet.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Uppdatera alla fält för att visa deras korrekta resultat.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

### Se även

* class [FieldQuote](../)
* namnutrymme [Aspose.Words.Fields](../../fieldquote/)
* hopsättning [Aspose.Words](../../../)


