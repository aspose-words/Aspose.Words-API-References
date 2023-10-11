---
title: FieldComments.Text
second_title: Aspose.Words für .NET-API-Referenz
description: FieldComments eigendom. Ruft den Text der Kommentare ab oder setzt ihn.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldcomments/text/
---
## FieldComments.Text property

Ruft den Text der Kommentare ab oder setzt ihn.

```csharp
public string Text { get; set; }
```

### Beispiele

Zeigt, wie das Feld KOMMENTARE verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Legen Sie einen Wert für die integrierte Eigenschaft „Kommentare“ des Dokuments fest.
doc.BuiltInDocumentProperties.Comments = "My comment.";

// Erstellen Sie ein COMMENTS-Feld, um den Wert dieser integrierten Eigenschaft anzuzeigen.
FieldComments field = (FieldComments)builder.InsertField(FieldType.FieldComments, true);
field.Update();

Assert.AreEqual(" COMMENTS ", field.GetFieldCode());
Assert.AreEqual("My comment.", field.Result);

// Wenn wir den Eigenschaftswert „Text“ des Felds „COMMENTS“ angeben und ihn aktualisieren, wird das Feld dies tun
// den aktuellen Wert der integrierten Eigenschaft „Comments“ mit dem Wert ihrer Text-Eigenschaft überschreiben,
// und dann den neuen Wert anzeigen.
field.Text = "My overriding comment.";
field.Update();

Assert.AreEqual(" COMMENTS  \"My overriding comment.\"", field.GetFieldCode());
Assert.AreEqual("My overriding comment.", field.Result);

doc.Save(ArtifactsDir + "Field.COMMENTS.docx");
```

### Siehe auch

* class [FieldComments](../)
* namensraum [Aspose.Words.Fields](../../fieldcomments/)
* Montage [Aspose.Words](../../../)


