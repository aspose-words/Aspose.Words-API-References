---
title: MailMerge.UnconditionalMergeFieldsAndRegions
linktitle: UnconditionalMergeFieldsAndRegions
articleTitle: UnconditionalMergeFieldsAndRegions
second_title: Aspose.Words per .NET
description: MailMerge UnconditionalMergeFieldsAndRegions proprietà. Ottiene o imposta un valore che indica se i campi e le aree di unione vengono uniti indipendentemente dalla condizione del campo IF padre in C#.
type: docs
weight: 140
url: /it/net/aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/
---
## MailMerge.UnconditionalMergeFieldsAndRegions property

Ottiene o imposta un valore che indica se i campi e le aree di unione vengono uniti indipendentemente dalla condizione del campo IF padre.

```csharp
public bool UnconditionalMergeFieldsAndRegions { get; set; }
```

## Osservazioni

Il valore predefinito è`falso` .

## Esempi

Mostra come unire campi o regioni indipendentemente dalla condizione del campo IF principale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce un MERGEFIELD nidificato all'interno di un campo IF.
// Poiché l'istruzione del campo IF è falsa, non verrà visualizzato il risultato di MERGEFIELD.
// Anche il MERGEFIELD non riceverà alcun dato durante una stampa unione.
FieldIf fieldIf = (FieldIf)builder.InsertField(" IF 1 = 2 ");
builder.MoveTo(fieldIf.Separator);
builder.InsertField(" MERGEFIELD  FullName ");

// Se impostiamo il flag "UnconditionalMergeFieldsAndRegions" su "true",
// la nostra stampa unione inserirà i dati nei campi non visualizzati come il nostro MERGEFIELD e tutti gli altri.
// Se impostiamo il flag "UnconditionalMergeFieldsAndRegions" su "false",
// la nostra stampa unione non inserirà i dati nei MERGEFIELD nascosti dai campi IF con false dichiarazioni.
doc.MailMerge.UnconditionalMergeFieldsAndRegions = countAllMergeFields;

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FullName");
dataTable.Rows.Add("James Bond");

doc.MailMerge.Execute(dataTable);

doc.Save(ArtifactsDir + "MailMerge.UnconditionalMergeFieldsAndRegions.docx");

Assert.AreEqual(
    countAllMergeFields
        ? "\u0013 IF 1 = 2 \"James Bond\"\u0014\u0015"
        : "\u0013 IF 1 = 2 \u0013 MERGEFIELD  FullName \u0014«FullName»\u0015\u0014\u0015",
    doc.GetText().Trim());
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
