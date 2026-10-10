---
title: "Aspose::Words::Fields::FieldOptions::get_CurrentUser método"
linktitle: "get_CurrentUser"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldOptions::get_CurrentUser método. Obtiene o establece la información del usuario actual en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.fields/fieldoptions/get_currentuser/
---
## FieldOptions::get_CurrentUser method


Obtiene o establece la información del usuario actual.

```cpp
const System::SharedPtr<Aspose::Words::Fields::UserInformation> & Aspose::Words::Fields::FieldOptions::get_CurrentUser() const
```


## Ejemplos



Muestra cómo establecer los detalles del usuario y mostrarlos usando campos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Cree un objeto UserInformation y configúrelo como la fuente de datos para los campos que muestran información del usuario.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
userInformation->set_Initials(u"J. D.");
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Inserte los campos USERNAME, USERINITIALS y USERADDRESS, que muestran valores de
// las respectivas propiedades del objeto UserInformation que hemos creado arriba.
ASSERT_EQ(userInformation->get_Name(), builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(userInformation->get_Initials(), builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(userInformation->get_Address(), builder->InsertField(u" USERADDRESS ")->get_Result());

// El objeto field options también tiene un usuario predeterminado estático al que los campos de todos los documentos pueden referirse.
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Name(u"Default User");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Initials(u"D. U.");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Address(u"One Microsoft Way");
doc->get_FieldOptions()->set_CurrentUser(Aspose::Words::Fields::UserInformation::get_DefaultUser());

ASSERT_EQ(u"Default User", builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(u"D. U.", builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(u"One Microsoft Way", builder->InsertField(u" USERADDRESS ")->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.CurrentUser.docx");
```

## Ver también

* Class [UserInformation](../../userinformation/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
