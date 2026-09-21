---
title: "Aspose::Words::Fields::FieldInfo::get_NewValue‑metod"
linktitle: "get_NewValue"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldInfo::get_NewValue‑metod. Hämtar eller anger ett valfritt värde som uppdaterar egenskapen i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.fields/fieldinfo/get_newvalue/
---
## FieldInfo::get_NewValue method


Hämtar eller anger ett valfritt värde som uppdaterar egenskapen.

```cpp
System::String Aspose::Words::Fields::FieldInfo::get_NewValue()
```


## Exempel



Visar hur man arbetar med INFO-fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ange ett värde för den inbyggda egenskapen "Comments" och infoga sedan ett INFO-fält för att visa den egenskapens värde.
doc->get_BuiltInDocumentProperties()->set_Comments(u"My comment");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldInfo>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->Update();

ASSERT_EQ(u" INFO  Comments", field->GetFieldCode());
ASSERT_EQ(u"My comment", field->get_Result());

builder->Writeln();

// Att ange ett värde för fältets NewValue-egenskap och uppdatera
// fältet kommer också att skriva över motsvarande inbyggda egenskap med det nya värdet.
field = System::ExplicitCast<Aspose::Words::Fields::FieldInfo>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->set_NewValue(u"New comment");
field->Update();

ASSERT_EQ(u" INFO  Comments \"New comment\"", field->GetFieldCode());
ASSERT_EQ(u"New comment", field->get_Result());
ASSERT_EQ(u"New comment", doc->get_BuiltInDocumentProperties()->get_Comments());

doc->Save(get_ArtifactsDir() + u"Field.INFO.docx");
```

## Se även

* Class [FieldInfo](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
