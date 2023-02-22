---
title: FieldQuote.Text
second_title: Aspose.Words für .NET-API-Referenz
description: FieldQuote eigendom. Ruft den abzurufenden Text ab oder legt ihn fest.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldquote/text/
---
## FieldQuote.Text property

Ruft den abzurufenden Text ab oder legt ihn fest.

```csharp
public string Text { get; set; }
```

### Beispiele

Zeigt die Verwendung des QUOTE-Felds an.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Füge ein QUOTE-Feld ein, das den Wert seiner Text-Eigenschaft anzeigt.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Ein QUOTE-Feld einfügen und ein DATE-Feld darin verschachteln.
// DATE-Felder aktualisieren ihren Wert jedes Mal auf das aktuelle Datum, wenn wir das Dokument mit Microsoft Word öffnen.
// Wenn Sie das DATE-Feld so in das QUOTE-Feld verschachteln, wird sein Wert eingefroren
// bis zu dem Datum, an dem wir das Dokument erstellt haben.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Aktualisieren Sie alle Felder, um ihre korrekten Ergebnisse anzuzeigen.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

### Siehe auch

* class [FieldQuote](../)
* namensraum [Aspose.Words.Fields](../../fieldquote/)
* Montage [Aspose.Words](../../../)


