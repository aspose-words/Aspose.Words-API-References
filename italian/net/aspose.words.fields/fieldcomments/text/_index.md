---
title: FieldComments.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words per .NET
description: Gestisci i tuoi commenti senza sforzo con la proprietà Testo FieldComments ottieni o imposta facilmente il testo del commento per una migliore interazione da parte dell'utente.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldcomments/text/
---
## FieldComments.Text property

Ottiene o imposta il testo dei commenti.

```csharp
public string Text { get; set; }
```

## Esempi

Mostra come utilizzare il campo COMMENTI.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Imposta un valore per la proprietà integrata "Commenti" del documento.
doc.BuiltInDocumentProperties.Comments = "My comment.";

// Crea un campo COMMENTI per visualizzare il valore di quella proprietà incorporata.
FieldComments field = (FieldComments)builder.InsertField(FieldType.FieldComments, true);
field.Update();

Assert.AreEqual(" COMMENTS ", field.GetFieldCode());
Assert.AreEqual("My comment.", field.Result);

// Se diamo il valore della proprietà Text del campo COMMENTS e lo aggiorniamo, il campo sarà
// sovrascrive il valore corrente della proprietà incorporata "Commenti" con il valore della sua proprietà Testo,
// e quindi visualizza il nuovo valore.
field.Text = "My overriding comment.";
field.Update();

Assert.AreEqual(" COMMENTS  \"My overriding comment.\"", field.GetFieldCode());
Assert.AreEqual("My overriding comment.", field.Result);

doc.Save(ArtifactsDir + "Field.COMMENTS.docx");
```

### Guarda anche

* class [FieldComments](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
