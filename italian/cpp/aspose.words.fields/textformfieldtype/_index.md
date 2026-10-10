---
title: "Aspose::Words::Fields::TextFormFieldType enum"
linktitle: "TextFormFieldType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::TextFormFieldType enum. Specifica il tipo di campo modulo di testo in C++."
type: docs
weight: 134000
url: /it/cpp/aspose.words.fields/textformfieldtype/
---
## TextFormFieldType enum


Specifica il tipo di un campo modulo di testo.

```cpp
enum class TextFormFieldType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Regolare | 0 | Il campo modulo di testo può contenere qualsiasi testo. |
| Number | 1 | Il campo modulo di testo può contenere solo numeri. |
| Data | 2 | Il campo modulo di testo può contenere solo un valore di data valido. |
| CurrentDate | 3 | Il valore del campo modulo di testo è la data corrente quando il campo viene aggiornato. |
| CurrentTime | 4 | Il valore del campo modulo di testo è l'ora corrente quando il campo viene aggiornato. |
| Calculated | 5 | Il valore del campo modulo di testo è calcolato dall'espressione specificata nella proprietà [TextInputDefault](../formfield/get_textinputdefault/). |


## Esempi



Mostra come creare campi modulo.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// I campi modulo sono oggetti nel documento con cui l'utente può interagire, venendo invitato a inserire valori.
// Possiamo crearli usando un costruttore di documenti, e di seguito sono riportati due modi per farlo.
// 1 -  Input di testo base:
builder->InsertTextInput(u"My text input", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Enter your name here", 30);

// 2 -  Casella combinata con testo di suggerimento e un intervallo di valori possibili:
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"-- Select your favorite footwear --", u"Sneakers", u"Oxfords", u"Flip-flops", u"Other"});

builder->InsertParagraph();
builder->InsertComboBox(u"My combo box", items, 0);

builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateForm.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
