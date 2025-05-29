---
title: TextColumnCollection.SetCount
linktitle: SetCount
articleTitle: SetCount
second_title: Aspose.Words per .NET
description: Ottimizza il tuo layout con il metodo TextColumnCollection SetCount, disponendo senza sforzo il testo nel numero di colonne desiderato per una migliore leggibilità.
type: docs
weight: 70
url: /it/net/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection.SetCount method

Dispone il testo nel numero specificato di colonne di testo.

```csharp
public void SetCount(int newCount)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| newCount | Int32 | Numero di colonne in cui deve essere disposto il testo. |

## Osservazioni

Quando[`EvenlySpaced`](../evenlyspaced/) È`falso` e aumenti il numero di colonne, nuovo[`TextColumn`](../../textcolumn/) gli oggetti vengono creati con larghezza e spaziatura zero. È necessario impostare larghezza e spaziatura per le nuove colonne.

## Esempi

Mostra come creare più colonne equidistanti in una sezione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### Guarda anche

* class [TextColumnCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
