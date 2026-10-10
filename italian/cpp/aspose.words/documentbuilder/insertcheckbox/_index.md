---
title: "Aspose::Words::DocumentBuilder::InsertCheckBox metodo"
linktitle: "InsertCheckBox"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder::InsertCheckBox metodo. Inserisce un campo modulo casella di controllo nella posizione corrente in C++."
type: docs
weight: 31000
url: /it/cpp/aspose.words/documentbuilder/insertcheckbox/
---
## DocumentBuilder::InsertCheckBox(const System::String\&, bool, int32_t) method


Inserisce un campo modulo casella di controllo nella posizione corrente.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertCheckBox(const System::String &name, bool checkedValue, int32_t size)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | const System::String\& | Il nome del campo modulo. Può essere una stringa vuota. Il valore più lungo di 20 caratteri verrà troncato. |
| checkedValue | bool | Stato selezionato della casella di controllo del campo modulo. |
| size | int32_t | Specifica la dimensione della casella di controllo in punti. Specificare 0 per MS Word per calcolare automaticamente la dimensione della casella di controllo. |

### ReturnValue

Il nodo del campo modulo appena inserito.
## Note


Se specifichi un nome per il campo modulo, viene automaticamente creato un segnalibro con lo stesso nome.

## Esempi



Mostra come inserire caselle di controllo nel documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci caselle di controllo di dimensioni variabili e stati selezionati predefiniti.
builder->Write(u"Unchecked check box of a default size: ");
builder->InsertCheckBox(System::String::Empty, false, false, 0);
builder->InsertParagraph();

builder->Write(u"Large checked check box: ");
builder->InsertCheckBox(u"CheckBox_Default", true, true, 50);
builder->InsertParagraph();

// I campi modulo hanno un limite di lunghezza del nome di 20 caratteri.
builder->Write(u"Very large checked check box: ");
builder->InsertCheckBox(u"CheckBox_OnlyCheckedValue", true, 100);

ASSERT_EQ(u"CheckBox_OnlyChecked", doc->get_Range()->get_FormFields()->idx_get(2)->get_Name());

// Possiamo interagire con queste caselle di controllo in Microsoft Word facendo doppio clic su di esse.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCheckBox.docx");
```

## Vedi anche

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertCheckBox(const System::String\&, bool, bool, int32_t) method


Inserisce un campo modulo casella di controllo nella posizione corrente.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertCheckBox(const System::String &name, bool defaultValue, bool checkedValue, int32_t size)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | const System::String\& | Il nome del campo modulo. Può essere una stringa vuota. Il valore più lungo di 20 caratteri verrà troncato. |
| defaultValue | bool | Valore predefinito del campo modulo casella di controllo. |
| checkedValue | bool | Stato attuale di selezione del campo modulo casella di controllo. |
| size | int32_t | Specifica la dimensione della casella di controllo in punti. Specificare 0 per MS Word per calcolare automaticamente la dimensione della casella di controllo. |

### ReturnValue

Il nodo del campo modulo appena inserito.
## Note


Se specifichi un nome per il campo modulo, viene automaticamente creato un segnalibro con lo stesso nome.

## Esempi



Mostra come inserire caselle di controllo nel documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci caselle di controllo di dimensioni variabili e stati selezionati predefiniti.
builder->Write(u"Unchecked check box of a default size: ");
builder->InsertCheckBox(System::String::Empty, false, false, 0);
builder->InsertParagraph();

builder->Write(u"Large checked check box: ");
builder->InsertCheckBox(u"CheckBox_Default", true, true, 50);
builder->InsertParagraph();

// I campi modulo hanno un limite di lunghezza del nome di 20 caratteri.
builder->Write(u"Very large checked check box: ");
builder->InsertCheckBox(u"CheckBox_OnlyCheckedValue", true, 100);

ASSERT_EQ(u"CheckBox_OnlyChecked", doc->get_Range()->get_FormFields()->idx_get(2)->get_Name());

// Possiamo interagire con queste caselle di controllo in Microsoft Word facendo doppio clic su di esse.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCheckBox.docx");
```

## Vedi anche

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
