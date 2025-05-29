---
title: FindReplaceOptions.SmartParagraphBreakReplacement
linktitle: SmartParagraphBreakReplacement
articleTitle: SmartParagraphBreakReplacement
second_title: Aspose.Words per .NET
description: Scopri la proprietà SmartParagraphBreakReplacement in FindReplaceOptions. Controlla le interruzioni di paragrafo senza sforzo per una formattazione del testo impeccabile.
type: docs
weight: 170
url: /it/net/aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/
---
## FindReplaceOptions.SmartParagraphBreakReplacement property

Ottiene o imposta un valore booleano che indica se è consentito sostituire il paragrafo break quando non esiste un paragrafo gemello successivo.

Il valore predefinito è`falso`.

```csharp
public bool SmartParagraphBreakReplacement { get; set; }
```

## Osservazioni

Questa opzione consente di sostituire l'interruzione di paragrafo quando non esiste un paragrafo gemello successivo in cui spostare tutti i nodi child , trovando qualsiasi paragrafo successivo (non necessariamente un paragrafo gemello) dopo il paragrafo che viene sostituito.

## Esempi

Mostra come rimuovere un paragrafo da una cella di una tabella con una tabella nidificata.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea una tabella con paragrafo e tabella interna nella prima cella.
builder.StartTable();
builder.InsertCell();
builder.Write("TEXT1");
builder.StartTable();
builder.InsertCell();
builder.EndTable();
builder.EndTable();
builder.Writeln();

FindReplaceOptions options = new FindReplaceOptions();
// Quando l'opzione seguente è impostata su 'true', Aspose.Words rimuoverà il testo del paragrafo
// completamente con il suo segno di paragrafo. Altrimenti, Aspose.Words imiterà Word e rimuoverà
// solo il testo del paragrafo e lascia intatto il segno di paragrafo (quando una tabella segue il testo).
options.SmartParagraphBreakReplacement = isSmartParagraphBreakReplacement;
doc.Range.Replace(new Regex(@"TEXT1&p"), "", options);

doc.Save(ArtifactsDir + "Table.RemoveParagraphTextAndMark.docx");
```

### Guarda anche

* class [FindReplaceOptions](../)
* spazio dei nomi [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assemblea [Aspose.Words](../../../)
