---
title: "Aspose::Words::Fields::Field::GetFieldCode metod"
linktitle: "GetFieldCode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::Field::GetFieldCode metod. Returnerar text mellan fältstart och fältseparator (eller fältslut om det inte finns någon separator). Både fältkod och fältresultat för underfält inkluderas i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words.fields/field/getfieldcode/
---
## Field::GetFieldCode() method


Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas.

```cpp
System::String Aspose::Words::Fields::Field::GetFieldCode()
```


## Exempel



Visar hur man infogar ett fält i ett dokument med en fältkod.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Denna överlagring av InsertField‑metoden uppdaterar automatiskt infogade fält.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```


Visar hur man hämtar ett fälts fältkod.
```cpp
// Öppna ett dokument som innehåller ett MERGEFIELD inuti ett IF‑fält.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Nested fields.docx");
auto fieldIf = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(doc->get_Range()->get_Fields()->idx_get(0));

// Det finns två sätt att hämta ett fälts fältkod:
// 1 -  Utelämna dess underfält:
ASSERT_EQ(u" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf->GetFieldCode(false));

// 2 -  Inkludera dess underfält:
ASSERT_EQ(System::String::Format(u" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" "), fieldIf->GetFieldCode(true));

// Som standard visar GetFieldCode‑metoden underfält.
ASSERT_EQ(fieldIf->GetFieldCode(), fieldIf->GetFieldCode(true));
```

## Se även

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## Field::GetFieldCode(bool) method


Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare).

```cpp
System::String Aspose::Words::Fields::Field::GetFieldCode(bool includeChildFieldCodes)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| includeChildFieldCodes | bool | **true** om underfältkod ska inkluderas. |

## Exempel



Visar hur man hämtar ett fälts fältkod.
```cpp
// Öppna ett dokument som innehåller ett MERGEFIELD inuti ett IF‑fält.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Nested fields.docx");
auto fieldIf = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(doc->get_Range()->get_Fields()->idx_get(0));

// Det finns två sätt att hämta ett fälts fältkod:
// 1 -  Utelämna dess underfält:
ASSERT_EQ(u" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf->GetFieldCode(false));

// 2 -  Inkludera dess underfält:
ASSERT_EQ(System::String::Format(u" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" "), fieldIf->GetFieldCode(true));

// Som standard visar GetFieldCode‑metoden underfält.
ASSERT_EQ(fieldIf->GetFieldCode(), fieldIf->GetFieldCode(true));
```

## Se även

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
