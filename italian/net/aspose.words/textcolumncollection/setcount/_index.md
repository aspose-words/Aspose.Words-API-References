---
title: TextColumnCollection.SetCount
linktitle: SetCount
articleTitle: SetCount
second_title: Aspose.Words per .NET
description: TextColumnCollection SetCount metodo. Dispone il testo nel numero specificato di colonne di testo in C#.
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
| newCount | Int32 | Il numero di colonne in cui deve essere organizzato il testo. |

## Osservazioni

Quando[`EvenlySpaced`](../evenlyspaced/) È`falso` e aumenti il numero di colonne, new[`TextColumn`](../../textcolumn/) gli oggetti vengono creati con larghezza e spaziatura pari a zero. È necessario impostare larghezza e spaziatura per le nuove colonne.

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
