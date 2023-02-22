---
title: FieldGoToButton.DisplayText
second_title: Aspose.Words per .NET API Reference
description: FieldGoToButton proprietà. Ottiene o imposta il testo del pulsante che compare nel documento in modo tale che possa essere selezionato per attivare il salto.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldgotobutton/displaytext/
---
## FieldGoToButton.DisplayText property

Ottiene o imposta il testo del "pulsante" che compare nel documento, in modo tale che possa essere selezionato per attivare il salto.

```csharp
public string DisplayText { get; set; }
```

### Esempi

Mostra per inserire un campo GOTOBUTTON.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aggiunge un campo GOTOBUTTON. Quando facciamo doppio clic su questo campo in Microsoft Word,
// porterà il cursore di testo sul segnalibro il cui nome fa riferimento alla proprietà Location.
FieldGoToButton field = (FieldGoToButton)builder.InsertField(FieldType.FieldGoToButton, true);
field.DisplayText = "My Button";
field.Location = "MyBookmark";

Assert.AreEqual(" GOTOBUTTON  MyBookmark My Button", field.GetFieldCode());

// Inserisce un segnalibro valido per il campo a cui fare riferimento.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark(field.Location);
builder.Writeln("Bookmark text contents.");
builder.EndBookmark(field.Location);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.GOTOBUTTON.docx");
```

### Guarda anche

* class [FieldGoToButton](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldgotobutton/)
* assemblea [Aspose.Words](../../../)


