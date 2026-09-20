---
title: "Método get_UserName de Aspose::Words::Fields::FieldUserName"
linktitle: "get_UserName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método get_UserName de Aspose::Words::Fields::FieldUserName. Obtiene o establece el nombre del usuario actual en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fieldusername/get_username/
---
## FieldUserName::get_UserName method


Obtiene o establece el nombre del usuario actual.

```cpp
System::String Aspose::Words::Fields::FieldUserName::get_UserName()
```


## Ejemplos



Muestra cómo usar el campo USERNAME.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Cree un objeto UserInformation y establézcalo como la fuente de información del usuario para cualquier campo que creemos.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Cree un campo USERNAME para mostrar el nombre del usuario actual,
// tomado del objeto UserInformation que creamos arriba.
auto fieldUserName = System::ExplicitCast<Aspose::Words::Fields::FieldUserName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserName, true));
ASSERT_EQ(userInformation->get_Name(), fieldUserName->get_Result());

ASSERT_EQ(u" USERNAME ", fieldUserName->GetFieldCode());
ASSERT_EQ(u"John Doe", fieldUserName->get_Result());

// Podemos establecer esta propiedad para que nuestro campo sobrescriba el valor almacenado actualmente en el objeto UserInformation.
fieldUserName->set_UserName(u"Jane Doe");
fieldUserName->Update();

ASSERT_EQ(u" USERNAME  \"Jane Doe\"", fieldUserName->GetFieldCode());
ASSERT_EQ(u"Jane Doe", fieldUserName->get_Result());

// Esto no afecta el valor en el objeto UserInformation.
ASSERT_EQ(u"John Doe", doc->get_FieldOptions()->get_CurrentUser()->get_Name());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERNAME.docx");
```

## Ver también

* Class [FieldUserName](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
