---
title: FieldTitle.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words per .NET
description: Gestisci la proprietà FieldTitle Text senza sforzo. Ottieni o imposta facilmente il testo del titolo per una maggiore chiarezza e un'esperienza utente migliore nella tua applicazione.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldtitle/text/
---
## FieldTitle.Text property

Ottiene o imposta il testo del titolo.

```csharp
public string Text { get; set; }
```

## Esempi

Mostra come utilizzare il campo TITLE.

```csharp
Document doc = new Document();

 // Imposta un valore per la proprietà incorporata del documento "Titolo".
doc.BuiltInDocumentProperties.Title = "My Title";

// Possiamo utilizzare il campo TITLE per visualizzare il valore di questa proprietà nel documento.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldTitle field = (FieldTitle)builder.InsertField(FieldType.FieldTitle, false);
field.Update();

Assert.AreEqual(" TITLE ", field.GetFieldCode());
Assert.AreEqual("My Title", field.Result);

// Impostazione di un valore per la proprietà Testo del campo,
// e quindi l'aggiornamento del campo sovrascriverà anche la proprietà incorporata corrispondente con il nuovo valore.
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

### Guarda anche

* class [FieldTitle](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
