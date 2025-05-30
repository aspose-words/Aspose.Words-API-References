---
title: FieldSubject.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words per .NET
description: Gestisci senza sforzo la proprietà Testo FieldSubject ottieni o imposta il testo dell'oggetto per una gestione dei dati ottimale e un'esperienza utente migliorata.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldsubject/text/
---
## FieldSubject.Text property

Ottiene o imposta il testo dell'oggetto.

```csharp
public string Text { get; set; }
```

## Esempi

Mostra come utilizzare il campo SOGGETTO.

```csharp
Document doc = new Document();

// Imposta un valore per la proprietà incorporata "Oggetto" del documento.
doc.BuiltInDocumentProperties.Subject = "My subject";

// Crea un campo SUBJECT per visualizzare il valore di quella proprietà incorporata.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldSubject field = (FieldSubject)builder.InsertField(FieldType.FieldSubject, true);
field.Update();

Assert.AreEqual(" SUBJECT ", field.GetFieldCode());
Assert.AreEqual("My subject", field.Result);

// Se forniamo il valore della proprietà Text del campo SUBJECT e lo aggiorniamo, il campo verrà
// sovrascrive il valore corrente della proprietà incorporata "Subject" con il valore della sua proprietà Text,
// e quindi visualizza il nuovo valore.
field.Text = "My new subject";
field.Update();

Assert.AreEqual(" SUBJECT  \"My new subject\"", field.GetFieldCode());
Assert.AreEqual("My new subject", field.Result);

Assert.AreEqual("My new subject", doc.BuiltInDocumentProperties.Subject);

doc.Save(ArtifactsDir + "Field.SUBJECT.docx");
```

### Guarda anche

* class [FieldSubject](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
