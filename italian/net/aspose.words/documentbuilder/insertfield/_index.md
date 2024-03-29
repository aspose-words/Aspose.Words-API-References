---
title: DocumentBuilder.InsertField
linktitle: InsertField
articleTitle: InsertField
second_title: Aspose.Words per .NET
description: DocumentBuilder InsertField metodo. Inserisce un campo Word in un documento e facoltativamente aggiorna il risultato del campo in C#.
type: docs
weight: 320
url: /it/net/aspose.words/documentbuilder/insertfield/
---
## InsertField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool*) {#insertfield}

Inserisce un campo Word in un documento e facoltativamente aggiorna il risultato del campo.

```csharp
public Field InsertField(FieldType fieldType, bool updateField)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldType | FieldType | Il tipo di campo da aggiungere. |
| updateField | Boolean | Specifica se aggiornare immediatamente il campo. |

### Valore di ritorno

UN[`Field`](../../../aspose.words.fields/field/) oggetto che rappresenta il campo inserito.

## Osservazioni

Questo metodo inserisce un campo in un documento. Aspose.Words può aggiornare i campi della maggior parte dei tipi, ma non tutti. Per maggiori dettagli vedere il `InsertField` sovraccarico.

## Esempi

Mostra come inserire un campo in un documento utilizzando FieldType.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce due campi passando un flag che determina se aggiornarli man mano che il builder li inserisce.
// In alcuni casi, l'aggiornamento dei campi potrebbe essere costoso dal punto di vista computazionale e potrebbe essere una buona idea posticipare l'aggiornamento.
doc.BuiltInDocumentProperties.Author = "John Doe";
builder.Write("This document was written by ");
builder.InsertField(FieldType.FieldAuthor, updateInsertedFieldsImmediately);

builder.InsertParagraph();
builder.Write("\nThis is page ");
builder.InsertField(FieldType.FieldPage, updateInsertedFieldsImmediately);

Assert.AreEqual(" AUTHOR ", doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(" PAGE ", doc.Range.Fields[1].GetFieldCode());

if (updateInsertedFieldsImmediately)
{
    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);
    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
else
{
    Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
    Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

    // Dovremo aggiornare manualmente questi campi utilizzando i metodi di aggiornamento.
    doc.Range.Fields[0].Update();

    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);

    doc.UpdateFields();

    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
```

### Guarda anche

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertField(*string*) {#insertfield_1}

Inserisce un campo Word in un documento e aggiorna il risultato del campo.

```csharp
public Field InsertField(string fieldCode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldCode | String | Il codice di campo da inserire (senza parentesi graffe). |

### Valore di ritorno

UN[`Field`](../../../aspose.words.fields/field/) oggetto che rappresenta il campo inserito.

## Osservazioni

Questo metodo inserisce un campo in un documento e aggiorna immediatamente il risultato del campo. Aspose.Words può aggiornare i campi della maggior parte dei tipi, ma non tutti. Per maggiori dettagli vedere il `InsertField` sovraccarico.

## Esempi

Mostra come inserire un campo in un documento utilizzando un codice di campo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Questo sovraccarico del metodo InsertField aggiorna automaticamente i campi inseriti.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

Mostra come inserire i campi e spostare su di essi il cursore del generatore di documenti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// Sposta il cursore sul primo MERGEFIELD.
builder.MoveToMergeField("MyMergeField1", true, false);

// Nota che il cursore viene posizionato immediatamente dopo il primo MERGEFIELD e prima del secondo.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// Se desideriamo modificare il codice o il contenuto del campo utilizzando il builder,
// il suo cursore dovrebbe trovarsi all'interno di un campo.
// Per posizionarlo all'interno di un campo, dovremmo chiamare il metodo MoveTo del generatore di documenti
// e passa il nodo iniziale o separatore del campo come argomento.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### Guarda anche

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertField(*string, string*) {#insertfield_2}

Inserisce un campo Word in un documento senza aggiornare il risultato del campo.

```csharp
public Field InsertField(string fieldCode, string fieldValue)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldCode | String | Il codice di campo da inserire (senza parentesi graffe). |
| fieldValue | String | Il valore del campo da inserire. Passaggio`nullo` per i campi che non hanno un valore. |

### Valore di ritorno

UN[`Field`](../../../aspose.words.fields/field/) oggetto che rappresenta il campo inserito.

## Osservazioni

I campi nei documenti Microsoft Word sono costituiti da un codice di campo e da un risultato di campo. Il codice di campo è come una formula e il risultato di campo è come il valore che produce la formula. Il codice di campo può anche contenere campi switch che sono come istruzioni aggiuntive per eseguire un'azione specifica.

Puoi passare dalla visualizzazione dei codici di campo ai risultati nel documento in Microsoft Word utilizzando la scorciatoia da tastiera Alt+F9. I codici di campo vengono visualizzati tra parentesi graffe ( { } ).

Per creare un campo, devi specificare un tipo di campo, un codice di campo e un valore di campo "segnaposto". Se non sei sicuro della sintassi di un particolare codice di campo, crea il campo in Microsoft Word first e passa a visualizzarne il codice di campo .

Aspose.Words può calcolare i risultati del campo per la maggior parte dei tipi di campo, ma questo metodo non aggiorna automaticamente il risultato del campo. Poiché il risultato del campo non viene calcolato automaticamente, è previsto che tu passi un valore di stringa (o anche una stringa vuota) che verrà inserito nel risultato del campo. Questo valore rimarrà nel risultato del campo come segnaposto finché il campo non sarà aggiornato. Per aggiornare il risultato del campo puoi chiamare[`Update`](../../../aspose.words.fields/field/update/)sull'oggetto campo restituito a te o[`UpdateFields`](../../document/updatefields/) per aggiornare i campi nell'intero documento.

## Esempi

Mostra come impostare la numerazione delle pagine in una sezione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 3.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("Section 2, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 3.");

// Sposta il generatore di documenti sull'intestazione principale della prima sezione,
// che verrà visualizzata in ogni pagina di quella sezione.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// Inserisci un campo PAGINA, che visualizzerà il numero della pagina corrente.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// Configura la sezione in modo che il conteggio delle pagine visualizzate nei campi PAGE inizi da 5.
// Inoltre, configura tutti i campi PAGE per visualizzare i relativi numeri di pagina utilizzando numeri romani maiuscoli.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// Crea un'altra intestazione primaria per la seconda sezione, con un altro campo PAGE.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// Configura la sezione in modo che il conteggio delle pagine visualizzate nei campi PAGE inizi da 10.
// Inoltre, configura tutti i campi PAGE per visualizzare i numeri di pagina utilizzando numeri arabi.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### Guarda anche

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
