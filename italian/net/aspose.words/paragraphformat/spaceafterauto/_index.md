---
title: ParagraphFormat.SpaceAfterAuto
linktitle: SpaceAfterAuto
articleTitle: SpaceAfterAuto
second_title: Aspose.Words per .NET
description: Scopri la proprietà ParagraphFormat SpaceAfterAuto. Regola automaticamente la spaziatura dei paragrafi per un layout del documento più pulito e professionale.
type: docs
weight: 320
url: /it/net/aspose.words/paragraphformat/spaceafterauto/
---
## ParagraphFormat.SpaceAfterAuto property

Vero se la quantità di spaziatura dopo il paragrafo viene impostata automaticamente.

```csharp
public bool SpaceAfterAuto { get; set; }
```

## Osservazioni

Quando impostato su`VERO` , annulla l'effetto di[`SpaceAfter`](../spaceafter/).

Quando imposti Spazio prima e Spazio dopo il paragrafo su Auto, Microsoft Word aggiunge automaticamente 14 punti di spaziatura tra i paragrafi in base alle seguenti regole:

* Solitamente la spaziatura viene aggiunta dopo tutti i paragrafi.
* In un elenco puntato o numerato, la spaziatura viene aggiunta solo dopo l'ultimo elemento dell'elenco. La spaziatura non viene aggiunta tra gli elementi dell'elenco.
* In un elenco puntato o numerato nidificato la spaziatura non viene aggiunta.
* Solitamente la spaziatura viene aggiunta dopo una tabella.
* La spaziatura non viene aggiunta dopo una tabella se questa è l'ultimo blocco in una cella di tabella.
* In una cella di tabella, la spaziatura non viene aggiunta dopo l'ultimo paragrafo.

## Esempi

Mostra come impostare la spaziatura automatica dei paragrafi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Applica una grande quantità di spaziatura prima e dopo i paragrafi che questo builder creerà.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Imposta questi flag su "true" per applicare la spaziatura automatica,
// ignorando di fatto la spaziatura nelle proprietà che abbiamo impostato sopra.
// Lasciandoli su "false" verrà applicata la nostra spaziatura personalizzata per i paragrafi.
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// Inserire due paragrafi con spaziatura sopra e sotto e salvare il documento.
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

### Guarda anche

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
