---
title: "Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat Methode"
linktitle: "get_UseInvariantCultureNumberFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat Methode. Gibt den Wert zurück oder legt ihn fest, der angibt, ob das Zahlenformat in C++ mit einer invarianten Kultur geparst wird oder nicht."
type: docs
weight: 21000
url: /de/cpp/aspose.words.fields/fieldoptions/get_useinvariantculturenumberformat/
---
## FieldOptions::get_UseInvariantCultureNumberFormat method


Liest oder legt den Wert fest, der angibt, ob das Zahlenformat mit Invariant Culture geparst wird oder nicht.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat() const
```

## Hinweise


Wenn diese Eigenschaft auf **true** gesetzt ist, wird das Zahlenformat aus einer invarianten Kultur übernommen.

Wenn diese Eigenschaft auf **false** gesetzt ist, wird das Zahlenformat aus der Kultur des aktuellen Threads übernommen.

Der Standardwert ist **false**.

## Beispiele



Zeigt, wie Zahlen gemäß der invarianten Kultur formatiert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::Threading::Thread::get_CurrentThread()->set_CurrentCulture(System::MakeObject<System::Globalization::CultureInfo>(u"de-DE"));
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" = 1234567,89 \\# $#,###,###.##");
field->Update();

// Manchmal formatieren Felder ihre Zahlen unter bestimmten Kulturen nicht korrekt.
ASSERT_FALSE(doc->get_FieldOptions()->get_UseInvariantCultureNumberFormat());
ASSERT_EQ(u"$1.234.567,89 ,     ", field->get_Result());

// Um dies zu beheben, könnten wir die Kultur für den gesamten Thread ändern.
// Eine andere Möglichkeit, dies zu beheben, besteht darin, dieses Flag zu setzen,
// was dafür sorgt, dass alle Felder bei der Zahlenformatierung die invariante Kultur verwenden.
// Auf diese Weise können wir das Ändern der Kultur für den gesamten Thread vermeiden.
doc->get_FieldOptions()->set_UseInvariantCultureNumberFormat(true);
field->Update();
ASSERT_EQ(u"$1.234.567,89", field->get_Result());
```

## Siehe auch

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
