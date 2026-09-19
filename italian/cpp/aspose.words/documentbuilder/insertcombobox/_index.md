---
title: "Aspose::Words::DocumentBuilder::InsertComboBox method"
linktitle: "InsertComboBox"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder::InsertComboBox method. Inserisce un campo modulo combobox nella posizione corrente in C++."
type: docs
weight: 32000
url: /it/cpp/aspose.words/documentbuilder/insertcombobox/
---
## DocumentBuilder::InsertComboBox method


Inserisce un campo modulo casella combinata nella posizione corrente.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertComboBox(const System::String &name, const System::ArrayPtr<System::String> &items, int32_t selectedIndex)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | const System::String\& | Il nome del campo modulo. Può essere una stringa vuota. Il valore più lungo di 20 caratteri verrà troncato. |
| items | const System::ArrayPtr\<System::String\>\& | Gli elementi della ComboBox. Il massimo è 25 elementi. |
| selectedIndex | int32_t | L'indice dell'elemento selezionato nella ComboBox. |

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


Mostra come inserire un campo modulo combo box in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un modulo che richiede all'utente di scegliere uno degli elementi dal menu.
builder->Write(u"Pick a fruit: ");
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"});
builder->InsertComboBox(u"DropDown", items, 0);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertComboBox.docx");
```

## Vedi anche

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
