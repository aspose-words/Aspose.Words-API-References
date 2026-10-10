---
title: "Aspose::Words::Fields::FormField::get_Result metod"
linktitle: "get_Result"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FormField::get_Result metod. Hämtar eller anger en sträng som representerar resultatet av detta formulärfält i C++."
type: docs
weight: 19000
url: /sv/cpp/aspose.words.fields/formfield/get_result/
---
## FormField::get_Result method


Hämtar eller anger en sträng som representerar resultatet av detta formulärfält.

```cpp
System::String Aspose::Words::Fields::FormField::get_Result()
```

## Anmärkningar


För ett textformulärfält är resultatet den text som finns i fältet.

För ett kryssrutfält kan resultatet vara "1" eller "0" för att indikera markerat eller omarkerat.

För ett rullgardinsformulärfält är resultatet den sträng som är markerad i rullgardinen.

Att ange [Result](./) för ett textformulärfält tillämpas inte den textformat som anges i [TextInputFormat](../get_textinputformat/). Om du vill ange ett värde och tillämpa formatet, använd metoden [SetTextInputValue()](../).

För ett textformulärfält tillämpas värdet [TextInputDefault](../get_textinputdefault/) om *value* är **null**.

## Exempel



Visar hur man infogar en kombinationsruta.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// Infoga en kombinationsruta som låter en användare välja ett alternativ från en samling strängar.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"}), 0);

ASSERT_EQ(u"MyComboBox", comboBox->get_Name());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldFormDropDown, comboBox->get_Type());
ASSERT_EQ(u"Apple", comboBox->get_Result());

// Formulärfältet kommer att visas i form av en "select"-HTML-tagg.
doc->Save(get_ArtifactsDir() + u"FormFields.Create.html");
```

## Se även

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
