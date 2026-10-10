---
title: "Aspose::Words::Fields::Field::GetFieldCode-Methode"
linktitle: "GetFieldCode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::Field::GetFieldCode-Methode. Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder das Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern sind in C++ enthalten."
type: docs
weight: 14000
url: /de/cpp/aspose.words.fields/field/getfieldcode/
---
## Field::GetFieldCode() method


Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldresultat von untergeordneten Feldern sind enthalten.

```cpp
System::String Aspose::Words::Fields::Field::GetFieldCode()
```


## Beispiele



Zeigt, wie man ein Feld mithilfe eines Feldcodes in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Diese Überladung der InsertField-Methode aktualisiert eingefügte Felder automatisch.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```


Zeigt, wie man den Feldcode eines Feldes erhält.
```cpp
// Öffnen Sie ein Dokument, das ein MERGEFIELD innerhalb eines IF-Feldes enthält.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Nested fields.docx");
auto fieldIf = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(doc->get_Range()->get_Fields()->idx_get(0));

// Es gibt zwei Möglichkeiten, den Feldcode eines Feldes zu erhalten:
// 1 -  Ignorieren Sie seine inneren Felder:
ASSERT_EQ(u" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf->GetFieldCode(false));

// 2 -  Schließen Sie seine inneren Felder ein:
ASSERT_EQ(System::String::Format(u" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" "), fieldIf->GetFieldCode(true));

// Standardmäßig zeigt die GetFieldCode-Methode innere Felder an.
ASSERT_EQ(fieldIf->GetFieldCode(), fieldIf->GetFieldCode(true));
```

## Siehe auch

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## Field::GetFieldCode(bool) method


Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist).

```cpp
System::String Aspose::Words::Fields::Field::GetFieldCode(bool includeChildFieldCodes)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| includeChildFieldCodes | bool | **true** wenn Kindfeldcodes eingeschlossen werden sollen. |

## Beispiele



Zeigt, wie man den Feldcode eines Feldes erhält.
```cpp
// Öffnen Sie ein Dokument, das ein MERGEFIELD innerhalb eines IF-Feldes enthält.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Nested fields.docx");
auto fieldIf = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(doc->get_Range()->get_Fields()->idx_get(0));

// Es gibt zwei Möglichkeiten, den Feldcode eines Feldes zu erhalten:
// 1 -  Ignorieren Sie seine inneren Felder:
ASSERT_EQ(u" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf->GetFieldCode(false));

// 2 -  Schließen Sie seine inneren Felder ein:
ASSERT_EQ(System::String::Format(u" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" "), fieldIf->GetFieldCode(true));

// Standardmäßig zeigt die GetFieldCode-Methode innere Felder an.
ASSERT_EQ(fieldIf->GetFieldCode(), fieldIf->GetFieldCode(true));
```

## Siehe auch

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
