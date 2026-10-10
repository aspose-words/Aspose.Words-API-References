---
title: "Aspose::Words::Fields::FieldInfo::get_InfoType método"
linktitle: "get_InfoType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldInfo::get_InfoType método. Obtiene o establece el tipo de la propiedad del documento a insertar en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fieldinfo/get_infotype/
---
## FieldInfo::get_InfoType method


Obtiene o establece el tipo de la propiedad del documento a insertar.

```cpp
System::String Aspose::Words::Fields::FieldInfo::get_InfoType()
```


## Ejemplos



Muestra cómo trabajar con campos INFO.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Establezca un valor para la propiedad incorporada \"Comments\" y luego inserte un campo INFO para mostrar el valor de esa propiedad.
doc->get_BuiltInDocumentProperties()->set_Comments(u"My comment");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldInfo>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->Update();

ASSERT_EQ(u" INFO  Comments", field->GetFieldCode());
ASSERT_EQ(u"My comment", field->get_Result());

builder->Writeln();

// Estableciendo un valor para la propiedad NewValue del campo y actualizando
// el campo también sobrescribirá la propiedad incorporada correspondiente con el nuevo valor.
field = System::ExplicitCast<Aspose::Words::Fields::FieldInfo>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->set_NewValue(u"New comment");
field->Update();

ASSERT_EQ(u" INFO  Comments \"New comment\"", field->GetFieldCode());
ASSERT_EQ(u"New comment", field->get_Result());
ASSERT_EQ(u"New comment", doc->get_BuiltInDocumentProperties()->get_Comments());

doc->Save(get_ArtifactsDir() + u"Field.INFO.docx");
```

## Ver también

* Class [FieldInfo](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
