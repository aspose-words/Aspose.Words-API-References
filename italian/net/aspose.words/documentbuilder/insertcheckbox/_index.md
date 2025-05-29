---
title: DocumentBuilder.InsertCheckBox
linktitle: InsertCheckBox
articleTitle: InsertCheckBox
second_title: Aspose.Words per .NET
description: Aggiungi senza sforzo campi modulo con caselle di controllo interattive con il metodo InsertCheckBox di DocumentBuilder, migliorando il coinvolgimento degli utenti nei tuoi documenti.
type: docs
weight: 290
url: /it/net/aspose.words/documentbuilder/insertcheckbox/
---
## InsertCheckBox(*string, bool, int*) {#insertcheckbox_1}

Inserisce un campo modulo casella di controllo nella posizione corrente.

```csharp
public FormField InsertCheckBox(string name, bool checkedValue, int size)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | String | Il nome del campo del modulo. Può essere una stringa vuota. I valori più lunghi di 20 caratteri verranno troncati. |
| checkedValue | Boolean | Stato verificato del campo del modulo della casella di controllo. |
| size | Int32 | Specifica la dimensione della casella di controllo in punti. Specificare 0 affinché MS Word calcoli automaticamente la dimensione della casella di controllo. |

### Valore di ritorno

Il nodo del campo modulo appena inserito.

## Osservazioni

Se si specifica un nome per il campo del modulo, verrà automaticamente creato un segnalibro con lo stesso nome.

## Esempi

Mostra come inserire caselle di controllo nel documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire caselle di controllo di diverse dimensioni e stati di selezione predefiniti.
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// I campi del modulo hanno un limite di lunghezza del nome di 20 caratteri.
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// Possiamo interagire con queste caselle di controllo in Microsoft Word facendo doppio clic su di esse.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertCheckBox.docx");
```

### Guarda anche

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertCheckBox(*string, bool, bool, int*) {#insertcheckbox}

Inserisce un campo modulo casella di controllo nella posizione corrente.

```csharp
public FormField InsertCheckBox(string name, bool defaultValue, bool checkedValue, int size)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | String | Il nome del campo del modulo. Può essere una stringa vuota. I valori più lunghi di 20 caratteri verranno troncati. |
| defaultValue | Boolean | Valore predefinito del campo modulo casella di controllo. |
| checkedValue | Boolean | Stato corrente di selezione del campo del modulo della casella di controllo. |
| size | Int32 | Specifica la dimensione della casella di controllo in punti. Specificare 0 affinché MS Word calcoli automaticamente la dimensione della casella di controllo. |

### Valore di ritorno

Il nodo del campo modulo appena inserito.

## Osservazioni

Se si specifica un nome per il campo del modulo, verrà automaticamente creato un segnalibro con lo stesso nome.

## Esempi

Mostra come inserire caselle di controllo nel documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire caselle di controllo di diverse dimensioni e stati di selezione predefiniti.
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// I campi del modulo hanno un limite di lunghezza del nome di 20 caratteri.
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// Possiamo interagire con queste caselle di controllo in Microsoft Word facendo doppio clic su di esse.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertCheckBox.docx");
```

### Guarda anche

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
