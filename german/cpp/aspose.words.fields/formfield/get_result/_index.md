---
title: "Aspose::Words::Fields::FormField::get_Result Methode"
linktitle: "get_Result"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FormField::get_Result Methode. Gibt einen String zurück oder legt ihn fest, der das Ergebnis dieses Formularfelds darstellt in C++."
type: docs
weight: 19000
url: /de/cpp/aspose.words.fields/formfield/get_result/
---
## FormField::get_Result method


Liest oder setzt eine Zeichenkette, die das Ergebnis dieses Formularfelds darstellt.

```cpp
System::String Aspose::Words::Fields::FormField::get_Result()
```

## Hinweise


Für ein Text-Formularfeld ist das Ergebnis der Text, der im Feld steht.

Für ein Kontrollkästchen-Formularfeld kann das Ergebnis "1" oder "0" sein, um aktiviert bzw. deaktiviert anzuzeigen.

Für ein Dropdown-Formularfeld ist das Ergebnis die im Dropdown ausgewählte Zeichenkette.

Das Festlegen von [Result](./) für ein Text-Formularfeld wendet das in [TextInputFormat](../get_textinputformat/) angegebene Textformat nicht an. Wenn Sie einen Wert festlegen und das Format anwenden möchten, verwenden Sie die Methode [SetTextInputValue()](../).

Für ein Text-Formularfeld wird der Wert [TextInputDefault](../get_textinputdefault/) angewendet, wenn *value* **null** ist.

## Beispiele



Zeigt, wie man ein Kombinationsfeld einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// Fügt ein Kombinationsfeld ein, das es einem Benutzer ermöglicht, eine Option aus einer Sammlung von Zeichenketten auszuwählen.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"}), 0);

ASSERT_EQ(u"MyComboBox", comboBox->get_Name());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldFormDropDown, comboBox->get_Type());
ASSERT_EQ(u"Apple", comboBox->get_Result());

// Das Formularfeld wird in Form eines "select"-HTML-Tags angezeigt.
doc->Save(get_ArtifactsDir() + u"FormFields.Create.html");
```

## Siehe auch

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
