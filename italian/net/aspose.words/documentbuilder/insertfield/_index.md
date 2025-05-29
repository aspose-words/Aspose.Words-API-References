---
title: DocumentBuilder.InsertField
linktitle: InsertField
articleTitle: InsertField
second_title: Aspose.Words per .NET
description: Migliora i tuoi documenti con il metodo InsertField di DocumentBuilder. Aggiungi e aggiorna facilmente i campi di Word per contenuti dinamici e funzionalità migliorate.
type: docs
weight: 330
url: /it/net/aspose.words/documentbuilder/insertfield/
---
## InsertField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool*) {#insertfield}

Inserisce un campo Word in un documento e, facoltativamente, aggiorna il risultato del campo.

```csharp
public Field InsertField(FieldType fieldType, bool updateField)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldType | FieldType | Tipo di campo da aggiungere. |
| updateField | Boolean | Specifica se aggiornare immediatamente il campo. |

### Valore di ritorno

UN[`Field`](../../../aspose.words.fields/field/) oggetto che rappresenta il campo inserito.

## Osservazioni

Questo metodo inserisce un campo in un documento. Aspose.Words può aggiornare campi della maggior parte dei tipi, ma non di tutti. Per maggiori dettagli, vedere `InsertField` sovraccarico.

## Esempi

Mostra come inserire un campo in un documento utilizzando FieldType.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce due campi passando un flag che determina se aggiornarli quando il builder li inserisce.
// In alcuni casi, l'aggiornamento dei campi potrebbe risultare dispendioso in termini di risorse computazionali e potrebbe essere una buona idea posticipare l'aggiornamento.
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
| fieldCode | String | Codice di campo da inserire (senza parentesi graffe). |

### Valore di ritorno

UN[`Field`](../../../aspose.words.fields/field/) oggetto che rappresenta il campo inserito.

## Osservazioni

Questo metodo inserisce un campo in un documento e ne aggiorna immediatamente il risultato. Aspose.Words può aggiornare campi della maggior parte dei tipi, ma non di tutti. Per maggiori dettagli, vedere `InsertField` sovraccarico.

## Esempi

Mostra come inserire un campo in un documento utilizzando un codice di campo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Questo sovraccarico del metodo InsertField aggiorna automaticamente i campi inseriti.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

Mostra come inserire campi e spostare su di essi il cursore del generatore di documenti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// Sposta il cursore sul primo MERGEFIELD.
builder.MoveToMergeField("MyMergeField1", true, false);

// Notare che il cursore viene posizionato immediatamente dopo il primo MERGEFIELD e prima del secondo.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// Se desideriamo modificare il codice del campo o il contenuto utilizzando il builder,
// il cursore dovrebbe trovarsi all'interno di un campo.
// Per inserirlo all'interno di un campo, dovremmo chiamare il metodo MoveTo del generatore di documenti
// e passare il nodo iniziale o separatore del campo come argomento.
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
| fieldCode | String | Codice di campo da inserire (senza parentesi graffe). |
| fieldValue | String | Il valore del campo da inserire. Passa`null` per i campi che non hanno un valore. |

### Valore di ritorno

UN[`Field`](../../../aspose.words.fields/field/) oggetto che rappresenta il campo inserito.

## Osservazioni

campi nei documenti di Microsoft Word sono costituiti da un codice di campo e da un risultato di campo. Il codice di campo è come una formula e il risultato di campo è come il valore prodotto dalla formula. Il codice di campo può anche contenere opzioni di campo che sono come istruzioni aggiuntive per eseguire un'azione specifica.

È possibile alternare la visualizzazione dei codici di campo e dei risultati nel documento in Microsoft Word utilizzando la combinazione di tasti Alt+F9. I codici di campo vengono visualizzati tra parentesi graffe ({}).

Per creare un campo, è necessario specificare un tipo di campo, un codice di campo e un valore di campo "segnaposto". Se non si è sicuri della sintassi di un particolare codice di campo, creare prima il campo in Microsoft Word e passare a visualizzarne il codice di campo.

Aspose.Words può calcolare i risultati dei campi per la maggior parte dei tipi di campo, ma questo metodo non aggiorna automaticamente il risultato del campo. Poiché il risultato del campo non viene calcolato automaticamente, è necessario passare un valore stringa (o anche una stringa vuota) che verrà inserito nel risultato del campo. Questo valore rimarrà nel risultato del campo come segnaposto finché il campo non verrà aggiornato. Per aggiornare il risultato del campo, è possibile chiamare[`Update`](../../../aspose.words.fields/field/update/) sul campo oggetto restituito a te o[`UpdateFields`](../../document/updatefields/) per aggiornare i campi dell'intero documento.

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

// Sposta il generatore di documenti nell'intestazione primaria della prima sezione,
// che verrà visualizzata in ogni pagina di quella sezione.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// Inserire un campo PAGINA, che visualizzerà il numero della pagina corrente.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// Configurare la sezione in modo che il conteggio delle pagine visualizzato nei campi PAGE parta da 5.
// Inoltre, configura tutti i campi PAGE in modo che visualizzino i numeri di pagina utilizzando numeri romani maiuscoli.
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

// Configurare la sezione in modo che il conteggio delle pagine visualizzato nei campi PAGE parta da 10.
// Inoltre, configura tutti i campi PAGE in modo che visualizzino i numeri di pagina utilizzando numeri arabi.
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
