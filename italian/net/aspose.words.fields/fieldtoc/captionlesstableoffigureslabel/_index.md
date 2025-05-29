---
title: FieldToc.CaptionlessTableOfFiguresLabel
linktitle: CaptionlessTableOfFiguresLabel
articleTitle: CaptionlessTableOfFiguresLabel
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldToc CaptionlessTableOfFiguresLabel per personalizzare il tuo indice delle figure. Gestisci facilmente gli identificatori di sequenza senza didascalie!
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldtoc/captionlesstableoffigureslabel/
---
## FieldToc.CaptionlessTableOfFiguresLabel property

Ottiene o imposta il nome dell'identificatore di sequenza utilizzato durante la creazione di una tabella di figure che non include l'etichetta e il numero della didascalia.

```csharp
public string CaptionlessTableOfFiguresLabel { get; set; }
```

## Esempi

Mostra come impostare il nome dell'identificatore di sequenza.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);
fieldToc.CaptionlessTableOfFiguresLabel = "Test";

Assert.AreEqual(" TOC  \\a Test", fieldToc.GetFieldCode());
```

### Guarda anche

* class [FieldToc](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
