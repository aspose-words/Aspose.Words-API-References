---
title: FieldKeywords.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words per .NET
description: Gestisci le tue FieldKeywords con facilità! Accedi e personalizza il testo delle parole chiave per prestazioni SEO ottimali e una maggiore visibilità.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldkeywords/text/
---
## FieldKeywords.Text property

Ottiene o imposta il testo delle parole chiave.

```csharp
public string Text { get; set; }
```

## Esempi

Mostra come inserire un campo PAROLE CHIAVE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aggiungere alcune parole chiave, chiamate anche "tag" in Esplora file.
doc.BuiltInDocumentProperties.Keywords = "Keyword1, Keyword2";

// Il campo PAROLE CHIAVE visualizza il valore di questa proprietà.
FieldKeywords field = (FieldKeywords)builder.InsertField(FieldType.FieldKeyword, true);
field.Update();

Assert.AreEqual(" KEYWORDS ", field.GetFieldCode());
Assert.AreEqual("Keyword1, Keyword2", field.Result);

// Impostazione di un valore per la proprietà Testo del campo,
// e quindi l'aggiornamento del campo sovrascriverà anche la proprietà incorporata corrispondente con il nuovo valore.
field.Text = "OverridingKeyword";
field.Update();

Assert.AreEqual(" KEYWORDS  OverridingKeyword", field.GetFieldCode());
Assert.AreEqual("OverridingKeyword", field.Result);
Assert.AreEqual("OverridingKeyword", doc.BuiltInDocumentProperties.Keywords);

doc.Save(ArtifactsDir + "Field.KEYWORDS.docx");
```

### Guarda anche

* class [FieldKeywords](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
