---
title: FieldTitle.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words für .NET
description: FieldTitle Text eigendom. Ruft den Text des Titels ab oder legt ihn fest in C#.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldtitle/text/
---
## FieldTitle.Text property

Ruft den Text des Titels ab oder legt ihn fest.

```csharp
public string Text { get; set; }
```

## Beispiele

Zeigt, wie das Feld TITLE verwendet wird.

```csharp
Document doc = new Document();

 // Legen Sie einen Wert für die integrierte Dokumenteigenschaft „Titel“ fest.
doc.BuiltInDocumentProperties.Title = "My Title";

// Wir können das TITLE-Feld verwenden, um den Wert dieser Eigenschaft im Dokument anzuzeigen.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldTitle field = (FieldTitle)builder.InsertField(FieldType.FieldTitle, false);
field.Update();

Assert.AreEqual(" TITLE ", field.GetFieldCode());
Assert.AreEqual("My Title", field.Result);

// Einen Wert für die Text-Eigenschaft des Feldes festlegen,
// und dann das Feld aktualisieren, wird auch die entsprechende integrierte Eigenschaft mit dem neuen Wert überschrieben.
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
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
