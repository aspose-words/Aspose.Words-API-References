---
title: "Aspose::Words::Fields::FieldUserAddress::get_UserAddress método"
linktitle: "get_UserAddress"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldUserAddress::get_UserAddress método. Obtiene o establece la dirección postal del usuario actual en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fielduseraddress/get_useraddress/
---
## FieldUserAddress::get_UserAddress method


Obtiene o establece la dirección postal del usuario actual.

```cpp
System::String Aspose::Words::Fields::FieldUserAddress::get_UserAddress()
```


## Ejemplos



Muestra cómo usar el campo USERADDRESS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Cree un objeto UserInformation y establézcalo como la fuente de información del usuario para cualquier campo que creemos.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Cree un campo USERADDRESS para mostrar la dirección del usuario actual,
// tomado del objeto UserInformation que creamos arriba.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto fieldUserAddress = System::ExplicitCast<Aspose::Words::Fields::FieldUserAddress>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserAddress, true));

ASSERT_EQ(u" USERADDRESS ", fieldUserAddress->GetFieldCode());
ASSERT_EQ(u"123 Main Street", fieldUserAddress->get_Result());

// Podemos establecer esta propiedad para que nuestro campo sobrescriba el valor almacenado actualmente en el objeto UserInformation.
fieldUserAddress->set_UserAddress(u"456 North Road");
fieldUserAddress->Update();

ASSERT_EQ(u" USERADDRESS  \"456 North Road\"", fieldUserAddress->GetFieldCode());
ASSERT_EQ(u"456 North Road", fieldUserAddress->get_Result());

// Esto no afecta el valor en el objeto UserInformation.
ASSERT_EQ(u"123 Main Street", doc->get_FieldOptions()->get_CurrentUser()->get_Address());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERADDRESS.docx");
```

## Ver también

* Class [FieldUserAddress](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
