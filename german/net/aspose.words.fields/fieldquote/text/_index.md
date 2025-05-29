---
title: FieldQuote.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words für .NET
description: FieldQuote-Texteigenschaft. Rufen Sie Text einfach ab oder legen Sie ihn fest, um die Datenverwaltung zu verbessern. Optimieren Sie Ihren Workflow mit dieser leistungsstarken Funktion!
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldquote/text/
---
## FieldQuote.Text property

Ruft den abzurufenden Text ab oder legt ihn fest.

```csharp
public string Text { get; set; }
```

## Beispiele

Zeigt die Verwendung des QUOTE-Felds.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein QUOTE-Feld ein, das den Wert seiner Texteigenschaft anzeigt.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Fügen Sie ein QUOTE-Feld ein und verschachteln Sie darin ein DATE-Feld.
// DATE-Felder aktualisieren ihren Wert jedes Mal auf das aktuelle Datum, wenn wir das Dokument mit Microsoft Word öffnen.
// Durch die Verschachtelung des Felds DATE in das Feld QUOTE wird sein Wert eingefroren
// bis zum Datum, an dem wir das Dokument erstellt haben.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Aktualisieren Sie alle Felder, um die korrekten Ergebnisse anzuzeigen.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

### Siehe auch

* class [FieldQuote](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
