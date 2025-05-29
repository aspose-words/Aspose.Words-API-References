---
title: FieldTC.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words per .NET
description: Gestisci la tua proprietà FieldTC Text senza sforzo. Ottieni o imposta facilmente il testo di inserimento per una gestione dei dati fluida e un'esperienza utente migliorata.
type: docs
weight: 40
url: /it/net/aspose.words.fields/fieldtc/text/
---
## FieldTC.Text property

Ottiene o imposta il testo della voce.

```csharp
public string Text { get; set; }
```

## Esempi

Mostra come inserire un campo TOC e filtrare quali campi TC vengono visualizzati come voci.

```csharp
public void FieldTocEntryIdentifier()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Inserire un campo TOC, che compilerà tutti i campi TC in un indice.
    FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Configurare il campo solo per raccogliere voci TC di tipo "A" e un livello di voce compreso tra 1 e 3.
    fieldToc.EntryIdentifier = "A";
    fieldToc.EntryLevelRange = "1-3";

    Assert.AreEqual(" TOC  \\f A \\l 1-3", fieldToc.GetFieldCode());

    // Queste due voci appariranno nella tabella.
    builder.InsertBreak(BreakType.PageBreak);
    InsertTocEntry(builder, "TC field 1", "A", "1");
    InsertTocEntry(builder, "TC field 2", "A", "2");

    Assert.AreEqual(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.Range.Fields[1].GetFieldCode());

    // Questa voce verrà omessa dalla tabella perché ha un tipo diverso da "A".
    InsertTocEntry(builder, "TC field 3", "B", "1");

    // Questa voce verrà omessa dalla tabella perché ha un livello di ingresso esterno all'intervallo 1-3.
    InsertTocEntry(builder, "TC field 4", "A", "5");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TC.docx");
}

/// <summary>
/// Utilizzare un generatore di documenti per inserire un campo TC.
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
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
