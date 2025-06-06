---
title: Paragraph.InsertField
linktitle: InsertField
articleTitle: InsertField
second_title: Aspose.Words per .NET
description: Inserisci facilmente campi nei paragrafi con il metodo Paragraph InsertField. Migliora la funzionalità del tuo documento e semplifica la gestione dei contenuti.
type: docs
weight: 290
url: /it/net/aspose.words/paragraph/insertfield/
---
## InsertField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool, [Node](../../node/), bool*) {#insertfield}

Inserisce un campo in questo paragrafo.

```csharp
public Field InsertField(FieldType fieldType, bool updateField, Node refNode, bool isAfter)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldType | FieldType | Il tipo di campo da inserire. |
| updateField | Boolean | Specifica se aggiornare immediatamente il campo. |
| refNode | Node | Nodo di riferimento all'interno di questo paragrafo (se*refNode* È`null`, quindi aggiunge alla fine del paragrafo). |
| isAfter | Boolean | Se inserire il campo dopo o prima del nodo di riferimento. |

### Valore di ritorno

UN[`Field`](../../../aspose.words.fields/field/) oggetto che rappresenta il campo inserito.

## Esempi

Mostra vari modi per aggiungere campi a un paragrafo.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Di seguito sono riportati tre modi per inserire un campo in un paragrafo.
// 1 - Inserire un campo AUTORE in un paragrafo dopo uno dei nodi figlio del paragrafo:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Inserire un campo QUOTE dopo uno dei nodi figlio del paragrafo:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Inserire un campo QUOTE prima di uno dei nodi figlio del paragrafo,
// e fagli visualizzare un valore segnaposto:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Questo campo visualizzerà il suo valore segnaposto finché non lo aggiorneremo.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Guarda anche

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [Node](../../node/)
* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertField(*string, [Node](../../node/), bool*) {#insertfield_1}

Inserisce un campo in questo paragrafo.

```csharp
public Field InsertField(string fieldCode, Node refNode, bool isAfter)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldCode | String | Codice di campo da inserire (senza parentesi graffe). |
| refNode | Node | Nodo di riferimento all'interno di questo paragrafo (se*refNode* È`null`, quindi aggiunge alla fine del paragrafo). |
| isAfter | Boolean | Se inserire il campo dopo o prima del nodo di riferimento. |

### Valore di ritorno

UN[`Field`](../../../aspose.words.fields/field/) oggetto che rappresenta il campo inserito.

## Esempi

Mostra vari modi per aggiungere campi a un paragrafo.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Di seguito sono riportati tre modi per inserire un campo in un paragrafo.
// 1 - Inserire un campo AUTORE in un paragrafo dopo uno dei nodi figlio del paragrafo:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Inserire un campo QUOTE dopo uno dei nodi figlio del paragrafo:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Inserire un campo QUOTE prima di uno dei nodi figlio del paragrafo,
// e fagli visualizzare un valore segnaposto:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Questo campo visualizzerà il suo valore segnaposto finché non lo aggiorneremo.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Guarda anche

* class [Field](../../../aspose.words.fields/field/)
* class [Node](../../node/)
* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertField(*string, string, [Node](../../node/), bool*) {#insertfield_2}

Inserisce un campo in questo paragrafo.

```csharp
public Field InsertField(string fieldCode, string fieldValue, Node refNode, bool isAfter)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldCode | String | Codice di campo da inserire (senza parentesi graffe). |
| fieldValue | String | Il valore del campo da inserire. Passa`null` per i campi che non hanno un valore. |
| refNode | Node | Nodo di riferimento all'interno di questo paragrafo (se*refNode* È`null`, quindi aggiunge alla fine del paragrafo). |
| isAfter | Boolean | Se inserire il campo dopo o prima del nodo di riferimento. |

### Valore di ritorno

UN[`Field`](../../../aspose.words.fields/field/) oggetto che rappresenta il campo inserito.

## Esempi

Mostra vari modi per aggiungere campi a un paragrafo.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Di seguito sono riportati tre modi per inserire un campo in un paragrafo.
// 1 - Inserire un campo AUTORE in un paragrafo dopo uno dei nodi figlio del paragrafo:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Inserire un campo QUOTE dopo uno dei nodi figlio del paragrafo:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Inserire un campo QUOTE prima di uno dei nodi figlio del paragrafo,
// e fagli visualizzare un valore segnaposto:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Questo campo visualizzerà il suo valore segnaposto finché non lo aggiorneremo.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Guarda anche

* class [Field](../../../aspose.words.fields/field/)
* class [Node](../../node/)
* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
