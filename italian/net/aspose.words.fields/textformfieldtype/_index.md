---
title: Enum TextFormFieldType
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Fields.TextFormFieldType enum. Specifica il tipo di un campo modulo di testo.
type: docs
weight: 2590
url: /it/net/aspose.words.fields/textformfieldtype/
---
## TextFormFieldType enumeration

Specifica il tipo di un campo modulo di testo.

```csharp
public enum TextFormFieldType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Regular | `0` | Il campo del modulo di testo può contenere qualsiasi testo. |
| Number | `1` | Il campo del modulo di testo può contenere solo numeri. |
| Date | `2` | Il campo del modulo di testo può contenere solo un valore di data valido. |
| CurrentDate | `3` | Il valore del campo del modulo di testo è la data corrente in cui il campo viene aggiornato. |
| CurrentTime | `4` | Il valore del campo del modulo di testo è l'ora corrente in cui il campo viene aggiornato. |
| Calculated | `5` | Il valore del campo del modulo di testo viene calcolato dall'espressione specificata in il[`TextInputDefault`](../formfield/textinputdefault/) proprietà. |

### Esempi

Mostra come creare campi modulo.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// I campi modulo sono oggetti nel documento con cui l'utente può interagire quando viene richiesto di immettere valori.
// Possiamo crearli utilizzando un generatore di documenti e di seguito sono riportati due modi per farlo.
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

* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)


