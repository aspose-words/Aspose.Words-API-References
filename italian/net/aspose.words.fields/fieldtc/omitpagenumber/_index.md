---
title: FieldTC.OmitPageNumber
second_title: Aspose.Words per .NET API Reference
description: FieldTC proprietà. Ottiene o imposta se il numero di pagina nel sommario deve essere omesso per questo campo.
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldtc/omitpagenumber/
---
## FieldTC.OmitPageNumber property

Ottiene o imposta se il numero di pagina nel sommario deve essere omesso per questo campo.

```csharp
public bool OmitPageNumber { get; set; }
```

### Esempi

Mostra come inserire un campo TOC e filtrare quali campi TC finiscono come voci.

```csharp
public void FieldTocEntryIdentifier()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Inserisci un campo TOC, che compilerà tutti i campi TC in un sommario.
    FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Configura il campo solo per raccogliere le voci TC del tipo "A" e un livello di ingresso compreso tra 1 e 3.
    fieldToc.EntryIdentifier = "A";
    fieldToc.EntryLevelRange = "1-3";

    Assert.AreEqual(" TOC  \\f A \\l 1-3", fieldToc.GetFieldCode());

    // Queste due voci appariranno nella tabella.
    builder.InsertBreak(BreakType.PageBreak);
    InsertTocEntry(builder, "TC field 1", "A", "1");
    InsertTocEntry(builder, "TC field 2", "A", "2");

    Assert.AreEqual(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.Range.Fields[1].GetFieldCode());

    // Questa voce verrà omessa dalla tabella perché è di tipo diverso da "A".
    InsertTocEntry(builder, "TC field 3", "B", "1");

    // Questa voce verrà omessa dalla tabella perché ha un livello di voce esterno all'intervallo 1-3.
    InsertTocEntry(builder, "TC field 4", "A", "5");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TC.docx");
}

/// <summary>
/// Utilizza un generatore di documenti per inserire un campo TC.
/// </summary>
public void InsertTocEntry(DocumentBuilder builder, string text, string typeIdentifier, string entryLevel)
{
    FieldTC fieldTc = (FieldTC)builder.InsertField(FieldType.FieldTOCEntry, true);
    fieldTc.OmitPageNumber = true;
    fieldTc.Text = text;
    fieldTc.TypeIdentifier = typeIdentifier;
    fieldTc.EntryLevel = entryLevel;
}
```

### Guarda anche

* class [FieldTC](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldtc/)
* assemblea [Aspose.Words](../../../)


