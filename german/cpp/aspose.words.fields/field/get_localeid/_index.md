---
title: "Aspose::Words::Fields::Field::get_LocaleId Methode"
linktitle: "get_LocaleId"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::Field::get_LocaleId Methode. Gibt die LCID des Feldes zurück oder setzt sie in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words.fields/field/get_localeid/
---
## Field::get_LocaleId method


Liefert oder setzt die LCID des Feldes.

```cpp
int32_t Aspose::Words::Fields::Field::get_LocaleId()
```


## Beispiele



Zeigt, wie man ein Feld einfügt und mit dessen Gebietsschema arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie ein DATE‑Feld ein und geben Sie anschließend das Datum aus, das angezeigt wird.
// Die aktuelle Kultur Ihres Threads bestimmt die Formatierung des Datums.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE");
std::cout << System::String::Format(u"Today's date, as displayed in the \"{0}\" culture: {1}", System::Globalization::CultureInfo::get_CurrentCulture()->get_EnglishName(), field->get_Result()) << std::endl;

ASSERT_EQ(1033, field->get_LocaleId());

// Das Ändern der Kultur unseres Threads wirkt sich auf das Ergebnis des DATE-Feldes aus.
// Eine weitere Möglichkeit, das DATE-Feld ein Datum in einer anderen Kultur anzeigen zu lassen, besteht darin, seine LocaleId‑Eigenschaft zu verwenden.
// Auf diese Weise können wir das Ändern der Thread‑Kultur vermeiden, um diesen Effekt zu erzielen.
doc->get_FieldOptions()->set_FieldUpdateCultureSource(Aspose::Words::Fields::FieldUpdateCultureSource::FieldCode);
auto de = System::MakeObject<System::Globalization::CultureInfo>(u"de-DE");
field->set_LocaleId(de->get_LCID());
field->Update();

std::cout << System::String::Format(u"Today's date, as displayed according to the \"{0}\" culture: {1}", System::Globalization::CultureInfo::GetCultureInfo(field->get_LocaleId())->get_EnglishName(), field->get_Result()) << std::endl;
```

## Siehe auch

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
