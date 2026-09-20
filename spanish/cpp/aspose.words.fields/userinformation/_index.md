---
title: "Aspose::Words::Fields::UserInformation class"
linktitle: "UserInformation"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::UserInformation class. Especifica información sobre el usuario. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 117000
url: /es/cpp/aspose.words.fields/userinformation/
---
## UserInformation class


Especifica información sobre el usuario. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class UserInformation : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Address](./get_address/)() const | Obtiene o establece la dirección postal del usuario. |
| static [get_DefaultUser](./get_defaultuser/)() | Información predeterminada del usuario. |
| [get_Initials](./get_initials/)() const | Obtiene o establece las iniciales del usuario. |
| [get_Name](./get_name/)() const | Obtiene o establece el nombre del usuario. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Address](./set_address/)(const System::String\&) | Método set para [Aspose::Words::Fields::UserInformation::get_Address](./get_address/). |
| [set_Initials](./set_initials/)(const System::String\&) | Método set para [Aspose::Words::Fields::UserInformation::get_Initials](./get_initials/). |
| [set_Name](./set_name/)(const System::String\&) | Método set para [Aspose::Words::Fields::UserInformation::get_Name](./get_name/). |
| static [Type](./type/)() |  |
| [UserInformation](./userinformation/)() |  |

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

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
