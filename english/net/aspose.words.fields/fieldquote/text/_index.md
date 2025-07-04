---
title: FieldQuote.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: FieldQuote Text property. Easily retrieve or set text for enhanced data management. Streamline your workflow with this powerful feature!
type: docs
weight: 20
url: /net/aspose.words.fields/fieldquote/text/
---
## FieldQuote.Text property

Gets or sets the text to retrieve.

```csharp
public string Text { get; set; }
```

## Examples

Shows to use the QUOTE field.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a QUOTE field, which will display the value of its Text property.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.That(field.GetFieldCode(), Is.EqualTo(" QUOTE  \"\\\"Quoted text\\\"\""));

// Insert a QUOTE field and nest a DATE field inside it.
// DATE fields update their value to the current date every time we open the document using Microsoft Word.
// Nesting the DATE field inside the QUOTE field like this will freeze its value
// to the date when we created the document.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.That(field.GetFieldCode(), Is.EqualTo(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015"));

// Update all the fields to display their correct results.
doc.UpdateFields();

Assert.That(doc.Range.Fields[0].Result, Is.EqualTo("\"Quoted text\""));

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

### See Also

* class [FieldQuote](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
