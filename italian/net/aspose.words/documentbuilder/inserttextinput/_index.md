---
title: DocumentBuilder.InsertTextInput
linktitle: InsertTextInput
articleTitle: InsertTextInput
second_title: Aspose.Words per .NET
description: Aggiungi facilmente campi di testo nei moduli con il metodo InsertTextInput di DocumentBuilder. Migliora l'interattività e l'esperienza utente del tuo documento oggi stesso!
type: docs
weight: 510
url: /it/net/aspose.words/documentbuilder/inserttextinput/
---
## DocumentBuilder.InsertTextInput method

Inserisce un campo modulo di testo nella posizione corrente.

```csharp
public FormField InsertTextInput(string name, TextFormFieldType type, string format, 
    string fieldValue, int maxLength)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | String | Il nome del campo del modulo. Può essere una stringa vuota. |
| type | TextFormFieldType | Specifica il tipo di campo del modulo di testo. |
| format | String | Stringa di formato utilizzata per formattare il valore del campo del modulo. |
| fieldValue | String | Testo che verrà mostrato nel campo. |
| maxLength | Int32 | Lunghezza massima che l'utente può inserire nel campo del modulo. Imposta a zero per una lunghezza illimitata. |

### Valore di ritorno

Il nodo del campo modulo appena inserito.

## Osservazioni

Se si specifica un nome per il campo del modulo, verrà automaticamente creato un segnalibro con lo stesso nome.

## Esempi

Mostra come inserire un campo modulo di immissione testo in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce un modulo che richiede all'utente di immettere del testo.
builder.InsertTextInput("TextInput", TextFormFieldType.Regular, "", "Enter your text here", 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTextInput.docx");
```

Mostra come inserire un campo di modulo di immissione testo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please enter text here: ");

// Inserisce un campo di immissione testo, che consentirà all'utente di cliccarci sopra e immettere testo.
// Assegna un testo segnaposto che l'utente può sovrascrivere e passare
// una lunghezza massima del testo pari a 0 per non applicare alcun limite al contenuto del campo del modulo.
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Il campo del modulo apparirà sotto forma di tag HTML "input", con tipo "testo".
doc.Save(ArtifactsDir + "FormFields.TextInput.html");
```

Mostra come creare campi modulo.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// I campi modulo sono oggetti nel documento con cui l'utente può interagire, chiedendogli di immettere valori.
// Possiamo crearli utilizzando un generatore di documenti. Di seguito sono riportati due metodi per farlo.
// 1 - Input di testo di base:
builder.InsertTextInput("My text input", TextFormFieldType.Regular, 
    "", "Enter your name here", 30);

// 2 - Casella combinata con testo di richiesta e un intervallo di valori possibili:
string[] items =
{
    "-- Select your favorite footwear --", "Sneakers", "Oxfords", "Flip-flops", "Other"
};

builder.InsertParagraph();
builder.InsertComboBox("My combo box", items, 0);

builder.Document.Save(ArtifactsDir + "DocumentBuilder.CreateForm.docx");
```

### Guarda anche

* class [FormField](../../../aspose.words.fields/formfield/)
* enum [TextFormFieldType](../../../aspose.words.fields/textformfieldtype/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
