---
title: HeightRule Enum
linktitle: HeightRule
articleTitle: HeightRule
second_title: Aspose.Words per .NET
description: Aspose.Words.HeightRule enum. Specifica la regola per determinare laltezza di un oggetto in C#.
type: docs
weight: 3130
url: /it/net/aspose.words/heightrule/
---
## HeightRule enumeration

Specifica la regola per determinare l'altezza di un oggetto.

```csharp
public enum HeightRule
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| AtLeast | `0` | L'altezza sarà almeno pari all'altezza specificata in punti. Crescerà, se necessario, per accogliere tutto il testo all'interno di un oggetto. |
| Exactly | `1` | L'altezza è specificata esattamente in punti. Tieni presente che se il testo non riesce a entrare nell'oggetto di questa altezza, apparirà troncato. |
| Auto | `2` | L'altezza aumenterà automaticamente per accogliere tutto il testo all'interno di un oggetto. |

## Esempi

Mostra come formattare le righe con un generatore di documenti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Inizia una seconda riga e quindi configura la sua altezza. Il builder applicherà queste impostazioni a
// la riga corrente, nonché le eventuali nuove righe create in seguito.
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// La prima riga non è stata influenzata dalla riconfigurazione del riempimento e mantiene ancora i valori predefiniti.
Assert.AreEqual(0.0d, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);

Assert.AreEqual(100.0d, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
