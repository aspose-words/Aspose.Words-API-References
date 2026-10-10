---
title: "Aspose::Words::Fields::FieldOptions::get_PreProcessCulture Methode"
linktitle: "get_PreProcessCulture"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldOptions::get_PreProcessCulture Methode. Ruft die Kultur ab oder legt sie fest, die zum Vorverarbeiten von Feldwerten in C++ verwendet wird."
type: docs
weight: 17000
url: /de/cpp/aspose.words.fields/fieldoptions/get_preprocessculture/
---
## FieldOptions::get_PreProcessCulture method


Liest oder setzt die Kultur zur Vorverarbeitung von Feldwerten.

```cpp
const System::SharedPtr<System::Globalization::CultureInfo> & Aspose::Words::Fields::FieldOptions::get_PreProcessCulture() const
```

## Hinweise


Derzeit wirkt sich diese Eigenschaft nur auf den Wert des [FieldDocProperty](../../fielddocproperty/) Feldes aus.

Der Standardwert ist **null**. Wenn diese Eigenschaft auf **null** gesetzt ist, wird der Wert des [FieldDocProperty](../../fielddocproperty/) Feldes mit der Kultur vorverarbeitet, die durch die Eigenschaft [FieldUpdateCultureSource](../get_fieldupdateculturesource/) gesteuert wird.

## Beispiele



Zeigt, wie man die Vorverarbeitungskultur festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Legen Sie die Kultur fest, nach der einige Felder ihre angezeigten Werte formatieren.
doc->get_FieldOptions()->set_PreProcessCulture(System::MakeObject<System::Globalization::CultureInfo>(u"de-DE"));

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" DOCPROPERTY CreateTime");

// Das DOCPROPERTY-Feld zeigt sein Ergebnis formatiert gemäß der Vorverarbeitungskultur an
// Wir haben sie auf Deutsch eingestellt. Das Feld zeigt das Datum/Uhrzeit im Format "dd.mm.yyyy hh:mm" an.
ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->get_Result(), u"\\d{2}[.]\\d{2}[.]\\d{4} \\d{2}[:]\\d{2}")->get_Success());

doc->get_FieldOptions()->set_PreProcessCulture(System::Globalization::CultureInfo::get_InvariantCulture());
field->Update();

// Nach dem Wechsel zur invarianten Kultur verwendet das DOCPROPERTY-Feld das Format "mm/dd/yyyy hh:mm".
ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->get_Result(), u"\\d{2}[/]\\d{2}[/]\\d{4} \\d{2}[:]\\d{2}")->get_Success());
```

## Siehe auch

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
