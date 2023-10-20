---
title: FieldSubject.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words für .NET
description: FieldSubject Text eigendom. Ruft den Text des Betreffs ab oder legt ihn fest in C#.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldsubject/text/
---
## FieldSubject.Text property

Ruft den Text des Betreffs ab oder legt ihn fest.

```csharp
public string Text { get; set; }
```

## Beispiele

Zeigt, wie das Feld SUBJECT verwendet wird.

```csharp
Document doc = new Document();

// Legen Sie einen Wert für die integrierte Eigenschaft „Subject“ des Dokuments fest.
doc.BuiltInDocumentProperties.Subject = "My subject";

// Erstellen Sie ein SUBJECT-Feld, um den Wert dieser integrierten Eigenschaft anzuzeigen.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldSubject field = (FieldSubject)builder.InsertField(FieldType.FieldSubject, true);
field.Update();

Assert.AreEqual(" SUBJECT ", field.GetFieldCode());
Assert.AreEqual("My subject", field.Result);

// Wenn wir den Text-Eigenschaftswert des SUBJECT-Felds angeben und ihn aktualisieren, wird das Feld dies tun
// den aktuellen Wert der integrierten Eigenschaft „Subject“ mit dem Wert ihrer Text-Eigenschaft überschreiben,
// und dann den neuen Wert anzeigen.
field.Text = "My new subject";
field.Update();

Assert.AreEqual(" SUBJECT  \"My new subject\"", field.GetFieldCode());
Assert.AreEqual("My new subject", field.Result);

Assert.AreEqual("My new subject", doc.BuiltInDocumentProperties.Subject);

doc.Save(ArtifactsDir + "Field.SUBJECT.docx");
```

### Siehe auch

* class [FieldSubject](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
