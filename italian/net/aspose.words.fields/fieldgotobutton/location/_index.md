---
title: FieldGoToButton.Location
linktitle: Location
articleTitle: Location
second_title: Aspose.Words per .NET
description: Scopri la proprietà Posizione FieldGoToButton, imposta facilmente segnalibri, numeri di pagina o elementi per una navigazione fluida e un'esperienza utente migliorata.
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldgotobutton/location/
---
## FieldGoToButton.Location property

Ottiene o imposta il nome di un segnalibro, un numero di pagina o un altro elemento a cui passare.

```csharp
public string Location { get; set; }
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
