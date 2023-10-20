---
title: FieldNextIf.LeftExpression
linktitle: LeftExpression
articleTitle: LeftExpression
second_title: Aspose.Words per .NET
description: FieldNextIf LeftExpression proprietà. Ottiene o imposta la parte sinistra dellespressione di confronto in C#.
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldnextif/leftexpression/
---
## FieldNextIf.LeftExpression property

Ottiene o imposta la parte sinistra dell'espressione di confronto.

```csharp
public string LeftExpression { get; set; }
```

## Esempi

Mostra come utilizzare i campi NEXT/NEXTIF per unire più righe in un'unica pagina durante una stampa unione.

```csharp
public void FieldNext()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Crea un'origine dati per la nostra stampa unione con 3 righe.
    // Una stampa unione che utilizza questa tabella creerebbe normalmente un documento di 3 pagine.
    DataTable table = new DataTable("Employees");
    table.Columns.Add("Courtesy Title");
    table.Columns.Add("First Name");
    table.Columns.Add("Last Name");
    table.Rows.Add("Mr.", "John", "Doe");
    table.Rows.Add("Mrs.", "Jane", "Cardholder");
    table.Rows.Add("Mr.", "Joe", "Bloggs");

    InsertMergeFields(builder, "First row: ");

    // Se abbiamo più campi di unione con lo stesso FieldName,
    // riceveranno i dati dalla stessa riga dell'origine dati e visualizzeranno lo stesso valore dopo l'unione.
    // Un campo NEXT indica immediatamente alla stampa unione di spostarsi di una riga verso il basso,
    // il che significa che tutti i MERGEFIELD che seguono il campo NEXT riceveranno i dati dalla riga successiva.
    // Assicurati di non provare mai a saltare alla riga successiva mentre sei già sull'ultima riga.
    FieldNext fieldNext = (FieldNext)builder.InsertField(FieldType.FieldNext, true);

    Assert.AreEqual(" NEXT ", fieldNext.GetFieldCode());

    // Dopo l'unione, i valori dell'origine dati accettati da questi MERGEFIELD
     // finirà sulla stessa pagina dei MERGEFIELD sopra.
    InsertMergeFields(builder, "Second row: ");

    // Un campo NEXTIF ha la stessa funzione di un campo NEXT,
    // ma salta alla riga successiva solo se un'istruzione costruita dalle seguenti 3 proprietà è vera.
    FieldNextIf fieldNextIf = (FieldNextIf)builder.InsertField(FieldType.FieldNextIf, true);
    fieldNextIf.LeftExpression = "5";
    fieldNextIf.RightExpression = "2 + 3";
    fieldNextIf.ComparisonOperator = "=";

    Assert.AreEqual(" NEXTIF  5 = \"2 + 3\"", fieldNextIf.GetFieldCode());

    // Se il confronto affermato dal campo precedente è corretto,
    // i seguenti 3 campi di unione prenderanno i dati dalla terza riga.
    // Altrimenti, questi campi prenderanno nuovamente i dati dalla riga 2.
    InsertMergeFields(builder, "Third row: ");

    doc.MailMerge.Execute(table);

     // La nostra origine dati ha 3 righe e le abbiamo saltate due volte.
    // Il nostro documento di output avrà 1 pagina con i dati di tutte e 3 le righe.
    doc.Save(ArtifactsDir + "Field.NEXT.NEXTIF.docx");
}

/// <summary>
/// Utilizza un generatore di documenti per inserire MERGEFIELD per un'origine dati che contiene colonne denominate "Titolo di cortesia", "Nome" e "Cognome".
/// </summary>
public void InsertMergeFields(DocumentBuilder builder, string firstFieldTextBefore)
{
    InsertMergeField(builder, "Courtesy Title", firstFieldTextBefore, " ");
    InsertMergeField(builder, "First Name", null, " ");
    InsertMergeField(builder, "Last Name", null, null);
    builder.InsertParagraph();
}

/// <summary>
/// Utilizza un generatore di documenti per inserire un MERRGEFIELD con le proprietà specificate.
/// </summary>
public void InsertMergeField(DocumentBuilder builder, string fieldName, string textBefore, string textAfter)
{
    FieldMergeField field = (FieldMergeField) builder.InsertField(FieldType.FieldMergeField, true);
    field.FieldName = fieldName;
    field.TextBefore = textBefore;
    field.TextAfter = textAfter;
}
```

### Guarda anche

* class [FieldNextIf](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
