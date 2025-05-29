---
title: FieldOptions.ToaCategories
linktitle: ToaCategories
articleTitle: ToaCategories
second_title: Aspose.Words per .NET
description: Scopri FieldOptions ToaCategories. Gestisci e personalizza facilmente le categorie dell'indice delle fonti per una migliore organizzazione ed efficienza.
type: docs
weight: 200
url: /it/net/aspose.words.fields/fieldoptions/toacategories/
---
## FieldOptions.ToaCategories property

Ottiene o imposta la tabella delle categorie delle autorità.

```csharp
public ToaCategories ToaCategories { get; set; }
```

## Esempi

Mostra come specificare un set di categorie per i campi TOA.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// I campi TOA possono filtrare le voci in base alle categorie definite in questa raccolta.
ToaCategories toaCategories = new ToaCategories();
doc.FieldOptions.ToaCategories = toaCategories;

// Questa raccolta di categorie è dotata di valori predefiniti, che possiamo sovrascrivere con valori personalizzati.
Assert.AreEqual("Cases", toaCategories[1]);
Assert.AreEqual("Statutes", toaCategories[2]);

toaCategories[1] = "My Category 1";
toaCategories[2] = "My Category 2";

// Possiamo sempre accedere ai valori predefiniti tramite questa raccolta.
Assert.AreEqual("Cases", ToaCategories.DefaultCategories[1]);
Assert.AreEqual("Statutes", ToaCategories.DefaultCategories[2]);

// Inserisci 2 campi TOA. I campi TOA creano una voce per ogni campo TA nel documento.
// Utilizzare l'opzione "\c" per selezionare l'indice di una categoria dalla nostra raccolta.
// Con questa opzione, un campo TOA raccoglierà solo le voci dai campi TA che
// hanno anche un'opzione "\c" con un indice di categoria corrispondente. Ogni campo TOA visualizzerà anche
// il nome della categoria a cui punta l'opzione "\c".
builder.InsertField("TOA \\c 1 \\h", null);
builder.InsertField("TOA \\c 2 \\h", null);
builder.InsertBreak(BreakType.PageBreak);

// Inserisci voci TOA in 2 categorie. Il nostro primo campo TOA riceverà una voce,
// dal secondo campo TA il cui parametro "\c" punta anche alla prima categoria.
// Il secondo campo TOA conterrà due voci dagli altri due campi TA.
builder.InsertField("TA \\c 2 \\l \"entry 1\"");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertField("TA \\c 1 \\l \"entry 2\"");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertField("TA \\c 2 \\l \"entry 3\"");

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.TOA.Categories.docx");
```

### Guarda anche

* class [ToaCategories](../../toacategories/)
* class [FieldOptions](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
