---
title: FindReplaceOptions.SmartParagraphBreakReplacement
second_title: Aspose.Words per .NET API Reference
description: FindReplaceOptions proprietà. Ottiene o imposta un valore booleano che indica che è consentito sostituire il paragrafo break quando non è presente un paragrafo di pari livello successivo.
type: docs
weight: 140
url: /it/net/aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/
---
## FindReplaceOptions.SmartParagraphBreakReplacement property

Ottiene o imposta un valore booleano che indica che è consentito sostituire il paragrafo break quando non è presente un paragrafo di pari livello successivo.

Il valore predefinito è`falso`.

```csharp
public bool SmartParagraphBreakReplacement { get; set; }
```

### Osservazioni

Questa opzione permette di sostituire l'interruzione di paragrafo quando non c'è un paragrafo di pari livello successivo a cui possono essere spostati tutti i nodi figlio , trovando un paragrafo qualsiasi (non necessariamente fratello) successivo al paragrafo da sostituire.

### Esempi

Mostra come rimuovere un paragrafo da una cella di una tabella con una tabella nidificata.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea tabella con paragrafo e tabella interna nella prima cella.
builder.StartTable();
builder.InsertCell();
builder.Write("TEXT1");
builder.StartTable();
builder.InsertCell();
builder.EndTable();
builder.EndTable();
builder.Writeln();

FindReplaceOptions options = new FindReplaceOptions();
// Quando la seguente opzione è impostata su 'true', Aspose.Words rimuoverà il testo del paragrafo
// completamente con il suo segno di paragrafo. In caso contrario, Aspose.Words imiterà Word e rimuoverà
// solo il testo del paragrafo e lascia intatto il segno del paragrafo (quando una tabella segue il testo).
options.SmartParagraphBreakReplacement = isSmartParagraphBreakReplacement;
doc.Range.Replace(new Regex(@"TEXT1&p"), "", options);

doc.Save(ArtifactsDir + "Table.RemoveParagraphTextAndMark.docx");
```

### Guarda anche

* class [FindReplaceOptions](../)
* spazio dei nomi [Aspose.Words.Replacing](../../findreplaceoptions/)
* assemblea [Aspose.Words](../../../)


