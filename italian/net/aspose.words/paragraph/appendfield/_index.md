---
title: Paragraph.AppendField
linktitle: AppendField
articleTitle: AppendField
second_title: Aspose.Words per .NET
description: Arricchisci il tuo documento con il metodo Paragraph AppendField, aggiungendo senza problemi campi personalizzati ai paragrafi per una migliore organizzazione e chiarezza.
type: docs
weight: 260
url: /it/net/aspose.words/paragraph/appendfield/
---
## AppendField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool*) {#appendfield}

Aggiunge un campo a questo paragrafo.

```csharp
public Field AppendField(FieldType fieldType, bool updateField)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldType | FieldType | Tipo di campo da aggiungere. |
| updateField | Boolean | Specifica se aggiornare immediatamente il campo. |

### Valore di ritorno

UN[`Field`](../../../aspose.words.fields/field/) oggetto che rappresenta il campo aggiunto.

## Esempi

Mostra vari modi per aggiungere campi a un paragrafo.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Di seguito sono riportati tre modi per aggiungere un campo alla fine di un paragrafo.
// 1 - Aggiungi un campo DATA utilizzando un tipo di campo e quindi aggiornalo:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - Aggiungere un campo TIME utilizzando un codice campo:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Aggiungi un campo QUOTE utilizzando un codice di campo e fai in modo che visualizzi un valore segnaposto:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Questo campo visualizzerà il suo valore segnaposto finché non lo aggiorneremo.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Guarda anche

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## AppendField(*string*) {#appendfield_1}

Aggiunge un campo a questo paragrafo.

```csharp
public Field AppendField(string fieldCode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldCode | String | Codice di campo da aggiungere (senza parentesi graffe). |

### Valore di ritorno

UN[`Field`](../../../aspose.words.fields/field/) oggetto che rappresenta il campo aggiunto.

## Esempi

Mostra vari modi per aggiungere campi a un paragrafo.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Di seguito sono riportati tre modi per aggiungere un campo alla fine di un paragrafo.
// 1 - Aggiungi un campo DATA utilizzando un tipo di campo e quindi aggiornalo:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - Aggiungere un campo TIME utilizzando un codice campo:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Aggiungi un campo QUOTE utilizzando un codice di campo e fai in modo che visualizzi un valore segnaposto:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Questo campo visualizzerà il suo valore segnaposto finché non lo aggiorneremo.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Guarda anche

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## AppendField(*string, string*) {#appendfield_2}

Aggiunge un campo a questo paragrafo.

```csharp
public Field AppendField(string fieldCode, string fieldValue)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldCode | String | Codice di campo da aggiungere (senza parentesi graffe). |
| fieldValue | String | Il valore del campo da aggiungere. Passa`null` per i campi che non hanno un valore. |

### Valore di ritorno

UN[`Field`](../../../aspose.words.fields/field/) oggetto che rappresenta il campo aggiunto.

## Esempi

Mostra vari modi per aggiungere campi a un paragrafo.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Di seguito sono riportati tre modi per aggiungere un campo alla fine di un paragrafo.
// 1 - Aggiungi un campo DATA utilizzando un tipo di campo e quindi aggiornalo:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - Aggiungere un campo TIME utilizzando un codice campo:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Aggiungi un campo QUOTE utilizzando un codice di campo e fai in modo che visualizzi un valore segnaposto:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Questo campo visualizzerà il suo valore segnaposto finché non lo aggiorneremo.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Guarda anche

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
