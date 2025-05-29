---
title: ParagraphFormat.SpaceAfter
linktitle: SpaceAfter
articleTitle: SpaceAfter
second_title: Aspose.Words per .NET
description: Controlla la spaziatura dei paragrafi con la proprietà SpaceAfter. Regola facilmente la spaziatura in punti per migliorare la leggibilità e la presentazione del tuo documento.
type: docs
weight: 310
url: /it/net/aspose.words/paragraphformat/spaceafter/
---
## ParagraphFormat.SpaceAfter property

Ottiene o imposta la quantità di spaziatura (in punti) dopo il paragrafo.

```csharp
public double SpaceAfter { get; set; }
```

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentOutOfRangeException | Generato quando l'argomento non rientra nell'intervallo di valori validi. |

## Osservazioni

Non ha effetto quando[`SpaceAfterAuto`](../spaceafterauto/) È`VERO`.

I valori validi vanno da 0 a 1584 inclusi.

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

Mostra come non applicare alcuna spaziatura tra paragrafi con lo stesso stile.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Applica una grande quantità di spaziatura prima e dopo i paragrafi che questo builder creerà.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Imposta il flag "NoSpaceBetweenParagraphsOfSameStyle" su "true" per applicare
// nessuna spaziatura tra paragrafi con lo stesso stile, che raggrupperà i paragrafi simili.
// Lascia il flag "NoSpaceBetweenParagraphsOfSameStyle" su "false"
// per applicare uniformemente la spaziatura a ogni paragrafo.
builder.ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle = noSpaceBetweenParagraphsOfSameStyle;

builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingSameStyle.docx");
```

### Guarda anche

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
