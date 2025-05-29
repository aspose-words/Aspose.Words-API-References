---
title: FieldGoToButton.DisplayText
linktitle: DisplayText
articleTitle: DisplayText
second_title: Aspose.Words per .NET
description: Personalizza la proprietà DisplayText del tuo FieldGoToButton per migliorare l'esperienza utente. Imposta facilmente il testo dei pulsanti per una navigazione fluida e un accesso rapido ai documenti.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldgotobutton/displaytext/
---
## FieldGoToButton.DisplayText property

Ottiene o imposta il testo del "pulsante" che appare nel documento, in modo che possa essere selezionato per attivare il salto.

```csharp
public string DisplayText { get; set; }
```

## Esempi

Mostra come inserire un campo GOTOBUTTON.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aggiungi un campo GOTOBUTTON. Facendo doppio clic su questo campo in Microsoft Word,
// porterà il cursore del testo sul segnalibro il cui nome è indicato dalla proprietà Location.
FieldGoToButton field = (FieldGoToButton)builder.InsertField(FieldType.FieldGoToButton, true);
field.DisplayText = "My Button";
field.Location = "MyBookmark";

Assert.AreEqual(" GOTOBUTTON  MyBookmark My Button", field.GetFieldCode());

// Inserire un segnalibro valido per il campo a cui fare riferimento.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark(field.Location);
builder.Writeln("Bookmark text contents.");
builder.EndBookmark(field.Location);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.GOTOBUTTON.docx");
```

### Guarda anche

* class [FieldGoToButton](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
