---
title: "Aspose::Words::Fields::FieldUserInitials::get_UserInitials método"
linktitle: "get_UserInitials"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldUserInitials::get_UserInitials método. Obtiene o establece las iniciales del usuario actual en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fielduserinitials/get_userinitials/
---
## FieldUserInitials::get_UserInitials method


Obtiene o establece las iniciales del usuario actual.

```cpp
System::String Aspose::Words::Fields::FieldUserInitials::get_UserInitials()
```


## Ejemplos



Muestra cómo usar el campo USERINITIALS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Cree un objeto UserInformation y establézcalo como la fuente de información del usuario para cualquier campo que creemos.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Initials(u"J. D.");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Cree un campo USERINITIALS para mostrar las iniciales del usuario actual,
// tomado del objeto UserInformation que creamos arriba.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto fieldUserInitials = System::ExplicitCast<Aspose::Words::Fields::FieldUserInitials>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserInitials, true));
ASSERT_EQ(userInformation->get_Initials(), fieldUserInitials->get_Result());

ASSERT_EQ(u" USERINITIALS ", fieldUserInitials->GetFieldCode());
ASSERT_EQ(u"J. D.", fieldUserInitials->get_Result());

// Podemos establecer esta propiedad para que nuestro campo sobrescriba el valor almacenado actualmente en el objeto UserInformation.
fieldUserInitials->set_UserInitials(u"J. C.");
fieldUserInitials->Update();

ASSERT_EQ(u" USERINITIALS  \"J. C.\"", fieldUserInitials->GetFieldCode());
ASSERT_EQ(u"J. C.", fieldUserInitials->get_Result());

// Esto no afecta el valor en el objeto UserInformation.
ASSERT_EQ(u"J. D.", doc->get_FieldOptions()->get_CurrentUser()->get_Initials());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERINITIALS.docx");
```

## Ver también

* Class [FieldUserInitials](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
