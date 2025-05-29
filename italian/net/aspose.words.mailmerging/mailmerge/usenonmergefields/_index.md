---
title: MailMerge.UseNonMergeFields
linktitle: UseNonMergeFields
articleTitle: UseNonMergeFields
second_title: Aspose.Words per .NET
description: Sfrutta la potenza di MailMerge! Utilizza la proprietà UseNonMergeFields per migliorare i tuoi documenti unendoli in vari tipi di campo in modo fluido.
type: docs
weight: 150
url: /it/net/aspose.words.mailmerging/mailmerge/usenonmergefields/
---
## MailMerge.UseNonMergeFields property

Quando`VERO` , specifica che oltre ai campi MERGEFIELD, la stampa unione viene eseguita in alcuni altri tipi di campi e anche nei tag "{{fieldName}}".

```csharp
public bool UseNonMergeFields { get; set; }
```

## Osservazioni

Normalmente, la stampa unione viene eseguita solo nei campi MERGEFIELD, ma diversi clienti avevano creato i propri reporting utilizzando altri campi e molti documenti in questo modo. Per semplificare la migrazione (e poiché questo approccio era utilizzato in modo indipendente da diversi clienti), è stata introdotta la possibilità di eseguire la stampa unione in altri campi.

Quando`UseNonMergeFields` è impostato su`VERO`Aspose.Words eseguirà la stampa unione nei seguenti campi:

MERGEFIELD Nome campo

MACROBUTTON NOMACRO FieldName

SE 0 = 0 "{NomeCampo}" ""

Inoltre, quando`UseNonMergeFields` è impostato su`VERO`Aspose.Words eseguirà la stampa unione nei tag di testo "{{fieldName}}". Questi non sono campi, ma solo tag di testo.

## Esempi

Mostra come preservare l'aspetto dei tag di stampa unione alternativi che non vengono utilizzati durante una stampa unione.

```csharp
public void PreserveUnusedTags(bool preserveUnusedTags)
{
    Document doc = CreateSourceDocWithAlternativeMergeFields();
    DataTable dataTable = CreateSourceTablePreserveUnusedTags();

     // Per impostazione predefinita, una stampa unione inserisce i dati di ogni riga di una tabella in campi MERGEFIELD, che assegnano un nome alle colonne di quella tabella.
    // Il nostro documento non ha campi di questo tipo, ma contiene tag di testo normale racchiusi tra parentesi graffe.
    // Se impostiamo il flag "PreserveUnusedTags" su "true", potremmo trattare questi tag come MERGEFIELD
    // per consentire alla nostra stampa unione di inserire dati dalla sorgente dati in quei tag.
    // Se impostiamo il flag "PreserveUnusedTags" su "false",
    // la stampa unione convertirà questi tag in MERGEFIELD e li lascerà vuoti.
    doc.MailMerge.PreserveUnusedTags = preserveUnusedTags;
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.PreserveUnusedTags.docx");

    // Il nostro documento ha un tag per una colonna denominata "Column2", che non esiste nella tabella.
    // Se impostiamo il flag "PreserveUnusedTags" su "false", then the mail merge will convert this tag into a MERGEFIELD.
    Assert.AreEqual(doc.GetText().Contains("{{ Column2 }}"), preserveUnusedTags);

    if (preserveUnusedTags)
        Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
    else
        Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
}

/// <summary>
/// Crea un documento e aggiungi due tag di testo normale che possono fungere da MERGEFIELD durante una stampa unione.
/// </summary>
private static Document CreateSourceDocWithAlternativeMergeFields()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("{{ Column1 }}");
    builder.Writeln("{{ Column2 }}");

    // I nostri tag verranno registrati come destinazioni per i dati di unione dati solo se impostiamo questo valore su true.
    doc.MailMerge.UseNonMergeFields = true;

    return doc;
}

/// <summary>
/// Crea una semplice tabella dati con una colonna.
/// </summary>
private static DataTable CreateSourceTablePreserveUnusedTags()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("Column1");
    dataTable.Rows.Add(new object[] { "Value1" });

    return dataTable;
}
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
