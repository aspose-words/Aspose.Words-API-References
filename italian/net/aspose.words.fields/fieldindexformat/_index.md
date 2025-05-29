---
title: FieldIndexFormat Enum
linktitle: FieldIndexFormat
articleTitle: FieldIndexFormat
second_title: Aspose.Words per .NET
description: Scopri l'enumerazione Aspose.Words.FieldIndexFormat per personalizzare la formattazione FieldIndex nei tuoi documenti. Migliora la struttura dei tuoi documenti senza sforzo!
type: docs
weight: 2480
url: /it/net/aspose.words.fields/fieldindexformat/
---
## FieldIndexFormat enumeration

Specifica la formattazione per il[`FieldIndex`](../fieldindex/) campi in un documento.

```csharp
public enum FieldIndexFormat
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Template | `0` | Dal modello. |
| Classic | `1` | Classico. |
| Fancy | `2` | Fantasia. |
| Modern | `3` | Moderno. |
| Bulleted | `4` | Con elenco puntato. |
| Formal | `5` | Formale. |
| Simple | `6` | Semplice. |

## Esempi

Mostra come formattare i campi FieldIndex.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("A");
builder.InsertBreak(BreakType.LineBreak);
builder.InsertField("XE \"A\"");
builder.Write("B");

builder.InsertField(" INDEX \\e \" · \" \\h \"A\" \\c \"2\" \\z \"1033\"", null);

doc.FieldOptions.FieldIndexFormat = FieldIndexFormat.Fancy;
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.SetFieldIndexFormat.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
