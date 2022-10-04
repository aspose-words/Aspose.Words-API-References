---
title: InsertField
second_title: Aspose.Words per .NET API Reference
description: Inserisce un campo in questo paragrafo.
type: docs
weight: 270
url: /it/net/aspose.words/paragraph/insertfield/
---
## InsertField(FieldType, bool, Node, bool) {#insertfield}

Inserisce un campo in questo paragrafo.

```csharp
public Field InsertField(FieldType fieldType, bool updateField, Node refNode, bool isAfter)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldType | FieldType | Il tipo di campo da inserire. |
| updateField | Boolean | Specifica se aggiornare il campo immediatamente. |
| refNode | Node | Nodo di riferimento all'interno di questo paragrafo (se refNode è null, viene aggiunto alla fine del paragrafo). |
| isAfter | Boolean | Se inserire il campo dopo o prima del nodo di riferimento. |

### Valore di ritorno

UN[`Field`](../../../aspose.words.fields/field/) oggetto che rappresenta il campo inserito.

### Esempi

Mostra vari modi per aggiungere campi a un paragrafo.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Di seguito sono riportati tre modi per inserire un campo in un paragrafo.
// 1 - Inserisci un campo AUTORE in un paragrafo dopo uno dei nodi figlio del paragrafo:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Inserisci un campo QUOTE dopo uno dei nodi figlio del paragrafo:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Inserisci un campo QUOTE prima di uno dei nodi figlio del paragrafo,
// e fallo visualizzare un valore segnaposto:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Questo campo mostrerà il suo valore segnaposto fino a quando non lo aggiorneremo.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Guarda anche

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [Node](../../node/)
* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../paragraph/)
* assemblea [Aspose.Words](../../../)

---

## InsertField(string, Node, bool) {#insertfield_1}

Inserisce un campo in questo paragrafo.

```csharp
public Field InsertField(string fieldCode, Node refNode, bool isAfter)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldCode | String | Il codice del campo da inserire (senza parentesi graffe). |
| refNode | Node | Nodo di riferimento all'interno di questo paragrafo (se refNode è null, viene aggiunto alla fine del paragrafo). |
| isAfter | Boolean | Se inserire il campo dopo o prima del nodo di riferimento. |

### Valore di ritorno

UN[`Field`](../../../aspose.words.fields/field/) oggetto che rappresenta il campo inserito.

### Esempi

Mostra vari modi per aggiungere campi a un paragrafo.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Di seguito sono riportati tre modi per inserire un campo in un paragrafo.
// 1 - Inserisci un campo AUTORE in un paragrafo dopo uno dei nodi figlio del paragrafo:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Inserisci un campo QUOTE dopo uno dei nodi figlio del paragrafo:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Inserisci un campo QUOTE prima di uno dei nodi figlio del paragrafo,
// e fallo visualizzare un valore segnaposto:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Questo campo mostrerà il suo valore segnaposto fino a quando non lo aggiorneremo.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Guarda anche

* class [Field](../../../aspose.words.fields/field/)
* class [Node](../../node/)
* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../paragraph/)
* assemblea [Aspose.Words](../../../)

---

## InsertField(string, string, Node, bool) {#insertfield_2}

Inserisce un campo in questo paragrafo.

```csharp
public Field InsertField(string fieldCode, string fieldValue, Node refNode, bool isAfter)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldCode | String | Il codice del campo da inserire (senza parentesi graffe). |
| fieldValue | String | Il valore del campo da inserire. Passa null per i campi che non hanno un valore. |
| refNode | Node | Nodo di riferimento all'interno di questo paragrafo (se refNode è null, viene aggiunto alla fine del paragrafo). |
| isAfter | Boolean | Se inserire il campo dopo o prima del nodo di riferimento. |

### Valore di ritorno

UN[`Field`](../../../aspose.words.fields/field/) oggetto che rappresenta il campo inserito.

### Esempi

Mostra vari modi per aggiungere campi a un paragrafo.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Di seguito sono riportati tre modi per inserire un campo in un paragrafo.
// 1 - Inserisci un campo AUTORE in un paragrafo dopo uno dei nodi figlio del paragrafo:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Inserisci un campo QUOTE dopo uno dei nodi figlio del paragrafo:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Inserisci un campo QUOTE prima di uno dei nodi figlio del paragrafo,
// e fallo visualizzare un valore segnaposto:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Questo campo mostrerà il suo valore segnaposto fino a quando non lo aggiorneremo.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Guarda anche

* class [Field](../../../aspose.words.fields/field/)
* class [Node](../../node/)
* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../paragraph/)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
