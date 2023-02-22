---
title: FieldTitle.Text
second_title: Aspose.Words für .NET-API-Referenz
description: FieldTitle eigendom. Liest oder setzt den Text des Titels.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldtitle/text/
---
## FieldTitle.Text property

Liest oder setzt den Text des Titels.

```csharp
public string Text { get; set; }
```

### Beispiele

Zeigt, wie das TITLE-Feld verwendet wird.

```csharp
Document doc = new Document();

 // Legen Sie einen Wert für die integrierte Dokumenteigenschaft "Title" fest.
doc.BuiltInDocumentProperties.Title = "My Title";

// Wir können das TITLE-Feld verwenden, um den Wert dieser Eigenschaft im Dokument anzuzeigen.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldTitle field = (FieldTitle)builder.InsertField(FieldType.FieldTitle, false);
field.Update();

Assert.AreEqual(" TITLE ", field.GetFieldCode());
Assert.AreEqual("My Title", field.Result);

// Festlegen eines Werts für die Text-Eigenschaft des Felds,
// und das anschließende Aktualisieren des Felds überschreibt auch die entsprechende integrierte Eigenschaft mit dem neuen Wert.
builder.Writeln();
field = (FieldTitle)builder.InsertField(FieldType.FieldTitle, false);
field.Text = "My New Title";
field.Update();

Assert.AreEqual(" TITLE  \"My New Title\"", field.GetFieldCode());
Assert.AreEqual("My New Title", field.Result);
Assert.AreEqual("My New Title", doc.BuiltInDocumentProperties.Title);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TITLE.docx");
```

### Siehe auch

* class [FieldTitle](../)
* namensraum [Aspose.Words.Fields](../../fieldtitle/)
* Montage [Aspose.Words](../../../)


