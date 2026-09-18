---
title: "Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat method"
linktitle: "get_LegacyNumberFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat method. Liest oder setzt den Wert, der angibt, ob das veraltete (vor AW 13.10) Zahlenformat für Felder in C++ aktiviert ist."
type: docs
weight: 16000
url: /de/cpp/aspose.words.fields/fieldoptions/get_legacynumberformat/
---
## FieldOptions::get_LegacyNumberFormat method


Liest oder setzt den Wert, der angibt, ob das veraltete (vor AW 13.10) Zahlenformat für Felder aktiviert ist oder nicht.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat() const
```

## Hinweise


Wenn diese Eigenschaft auf **true** gesetzt ist, funktioniert das Vorlagensymbol \"#\" wie in .net: Es ersetzt das Pfundzeichen durch die entsprechende Ziffer, falls vorhanden; andernfalls erscheint kein Symbol im Ergebnisstring.

Wenn diese Eigenschaft auf **false** gesetzt ist, funktioniert das Vorlagensymbol \"#\" wie in MS Word: Dieses Formatierungszeichen gibt die erforderlichen numerischen Stellen an, die im Ergebnis angezeigt werden sollen. Enthält das Ergebnis an dieser Stelle keine Ziffer, zeigt MS Word ein Leerzeichen an. Zum Beispiel zeigt { = 9 + 6 \\# $### } $ 15 an.

Der Standardwert ist **false**.

## Beispiele



Zeigt, wie man das veraltete Zahlenformat für Felder aktiviert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"= 2 + 3 \\# $##");

ASSERT_EQ(u"$ 5", field->get_Result());

doc->get_FieldOptions()->set_LegacyNumberFormat(true);
field->Update();

ASSERT_EQ(u"$5", field->get_Result());
```

## Siehe auch

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
