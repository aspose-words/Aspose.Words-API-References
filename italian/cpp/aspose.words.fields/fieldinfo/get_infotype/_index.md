---
title: "Aspose::Words::Fields::FieldInfo::get_InfoType metodo"
linktitle: "get_InfoType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldInfo::get_InfoType metodo. Ottiene o imposta il tipo della proprietà del documento da inserire in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldinfo/get_infotype/
---
## FieldInfo::get_InfoType method


Ottiene o imposta il tipo della proprietà del documento da inserire.

```cpp
System::String Aspose::Words::Fields::FieldInfo::get_InfoType()
```


## Esempi



Mostra come lavorare con i campi INFO.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Imposta un valore per la proprietà incorporata "Comments" e poi inserisci un campo INFO per visualizzare il valore di quella proprietà.
doc->get_BuiltInDocumentProperties()->set_Comments(u"My comment");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldInfo>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->Update();

ASSERT_EQ(u" INFO  Comments", field->GetFieldCode());
ASSERT_EQ(u"My comment", field->get_Result());

builder->Writeln();

// Impostare un valore per la proprietà NewValue del campo e aggiornare
// il campo sovrascriverà anche la proprietà incorporata corrispondente con il nuovo valore.
field = System::ExplicitCast<Aspose::Words::Fields::FieldInfo>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->set_NewValue(u"New comment");
field->Update();

ASSERT_EQ(u" INFO  Comments \"New comment\"", field->GetFieldCode());
ASSERT_EQ(u"New comment", field->get_Result());
ASSERT_EQ(u"New comment", doc->get_BuiltInDocumentProperties()->get_Comments());

doc->Save(get_ArtifactsDir() + u"Field.INFO.docx");
```

## Vedi anche

* Class [FieldInfo](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
