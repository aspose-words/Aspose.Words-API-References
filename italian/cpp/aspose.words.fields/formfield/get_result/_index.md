---
title: "Metodo Aspose::Words::Fields::FormField::get_Result"
linktitle: "get_Result"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FormField::get_Result. Ottiene o imposta una stringa che rappresenta il risultato di questo campo modulo in C++."
type: docs
weight: 19000
url: /it/cpp/aspose.words.fields/formfield/get_result/
---
## FormField::get_Result method


Ottiene o imposta una stringa che rappresenta il risultato di questo campo modulo.

```cpp
System::String Aspose::Words::Fields::FormField::get_Result()
```

## Note


Per un campo modulo di testo, il risultato è il testo presente nel campo.

Per un campo modulo di casella di controllo, il risultato può essere "1" o "0" per indicare selezionato o deselezionato.

Per un campo modulo a discesa, il risultato è la stringa selezionata nel menu a discesa.

Impostare [Result](./) per un campo modulo di testo non applica il formato del testo specificato in [TextInputFormat](../get_textinputformat/). Se desideri impostare un valore e applicare il formato, usa il metodo [SetTextInputValue()](../).

Per un campo modulo di testo, il valore [TextInputDefault](../get_textinputdefault/) viene applicato se *value* è **null**.

## Esempi



Mostra come inserire una casella combinata.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// Inserisci una casella combinata che consentirà all'utente di scegliere un'opzione da una raccolta di stringhe.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"}), 0);

ASSERT_EQ(u"MyComboBox", comboBox->get_Name());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldFormDropDown, comboBox->get_Type());
ASSERT_EQ(u"Apple", comboBox->get_Result());

// Il campo modulo apparirà sotto forma di tag html "select".
doc->Save(get_ArtifactsDir() + u"FormFields.Create.html");
```

## Vedi anche

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
