---
title: ParagraphFormat.SpaceAfterAuto
linktitle: SpaceAfterAuto
articleTitle: SpaceAfterAuto
second_title: Aspose.Words per .NET
description: ParagraphFormat SpaceAfterAuto proprietà. Vero se la quantità di spaziatura dopo il paragrafo viene impostata automaticamente in C#.
type: docs
weight: 310
url: /it/net/aspose.words/paragraphformat/spaceafterauto/
---
## ParagraphFormat.SpaceAfterAuto property

Vero se la quantità di spaziatura dopo il paragrafo viene impostata automaticamente.

```csharp
public bool SpaceAfterAuto { get; set; }
```

## Osservazioni

Quando impostato su`VERO` , sovrascrive l'effetto di[`SpaceAfter`](../spaceafter/).

Quando imposti Spazio prima e Spazio dopo su Auto, Microsoft Word aggiunge automaticamente 14 punti di spaziatura tra i paragrafi in base alle seguenti regole:

* Normalmente, la spaziatura viene aggiunta dopo tutti i paragrafi.
* In un elenco puntato o numerato, la spaziatura viene aggiunta solo dopo l'ultimo elemento dell'elenco. La spaziatura non viene aggiunta tra gli elementi dell'elenco.
* In un elenco puntato o numerato nidificato la spaziatura non viene aggiunta.
* La spaziatura viene normalmente aggiunta dopo una tabella.
* La spaziatura non viene aggiunta dopo una tabella se si tratta dell'ultimo blocco in una cella della tabella.
* La spaziatura non viene aggiunta dopo l'ultimo paragrafo in una cella di tabella.

## Esempi

Mostra come impostare la spaziatura automatica dei paragrafi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Applica una grande quantità di spaziatura prima e dopo i paragrafi che questo builder creerà.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Imposta questi flag su "true" per applicare la spaziatura automatica,
// ignorando di fatto la spaziatura nelle proprietà impostate sopra.
// Lasciarli come "falsi" applicherà la nostra spaziatura paragrafo personalizzata.
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// Inserisci due paragrafi che avranno uno spazio sopra e sotto e salva il documento.
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

### Guarda anche

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
