---
title: ParagraphFormat.SpaceBefore
second_title: Aspose.Words per .NET API Reference
description: ParagraphFormat proprietà. Ottiene o imposta la quantità di spaziatura in punti prima del paragrafo.
type: docs
weight: 320
url: /it/net/aspose.words/paragraphformat/spacebefore/
---
## ParagraphFormat.SpaceBefore property

Ottiene o imposta la quantità di spaziatura (in punti) prima del paragrafo.

```csharp
public double SpaceBefore { get; set; }
```

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentOutOfRangeException | Viene generato quando l'argomento non rientra nell'intervallo di valori validi. |

### Osservazioni

Non ha alcun effetto quando[`SpaceBeforeAuto`](../spacebeforeauto/) È`VERO`.

I valori validi vanno da 0 a 1584 inclusi.

### Esempi

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

Mostra come non applicare alcuna spaziatura tra i paragrafi con lo stesso stile.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Applica una grande quantità di spaziatura prima e dopo i paragrafi che questo builder creerà.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Imposta il flag "NoSpaceBetweenParagraphsOfSameStyle" su "true" per applicare
// nessuna spaziatura tra i paragrafi con lo stesso stile, che raggrupperà paragrafi simili.
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
* spazio dei nomi [Aspose.Words](../../paragraphformat/)
* assemblea [Aspose.Words](../../../)


