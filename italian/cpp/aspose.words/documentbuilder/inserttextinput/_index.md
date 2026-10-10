---
title: "Aspose::Words::DocumentBuilder::InsertTextInput method"
linktitle: "InsertTextInput"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder::InsertTextInput method. Inserisce un campo modulo di testo nella posizione corrente in C++."
type: docs
weight: 49000
url: /it/cpp/aspose.words/documentbuilder/inserttextinput/
---
## DocumentBuilder::InsertTextInput method


Inserisce un campo modulo di testo nella posizione corrente.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertTextInput(const System::String &name, Aspose::Words::Fields::TextFormFieldType type, const System::String &format, const System::String &fieldValue, int32_t maxLength)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | const System::String\& | Il nome del campo modulo. Può essere una stringa vuota. |
| tipo | Aspose::Words::Fields::TextFormFieldType | Specifica il tipo del campo modulo di testo. |
| formato | const System::String\& | Stringa di formato usata per formattare il valore del campo modulo. |
| fieldValue | const System::String\& | Testo che verrà mostrato nel campo. |
| maxLength | int32_t | Lunghezza massima che l'utente può inserire nel campo modulo. Imposta a zero per lunghezza illimitata. |

### ReturnValue

Il nodo del campo modulo appena inserito.
## Note


Se specifichi un nome per il campo modulo, viene automaticamente creato un segnalibro con lo stesso nome.

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


Mostra come inserire un campo modulo di input di testo in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un modulo che richiede all'utente di inserire del testo.
builder->InsertTextInput(u"TextInput", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Enter your text here", 0);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTextInput.docx");
```


Mostra come inserire un campo modulo di input di testo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please enter text here: ");

// Inserisci un campo di input di testo, che consentirà all'utente di cliccarci e inserire del testo.
// Assegna del testo segnaposto che l'utente può sovrascrivere e passare
// una lunghezza massima del testo pari a 0 per non applicare alcun limite al contenuto del campo modulo.
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// Il campo modulo apparirà sotto forma di un tag html "input", con un tipo "text".
doc->Save(get_ArtifactsDir() + u"FormFields.TextInput.html");
```

## Vedi anche

* Class [FormField](../../../aspose.words.fields/formfield/)
* Enum [TextFormFieldType](../../../aspose.words.fields/textformfieldtype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
