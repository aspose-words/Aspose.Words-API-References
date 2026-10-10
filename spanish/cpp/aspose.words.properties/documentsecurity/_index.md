---
title: "Enumeración Aspose::Words::Properties::DocumentSecurity"
linktitle: "DocumentSecurity"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Enumeración Aspose::Words::Properties::DocumentSecurity. Se usa como valor para la propiedad Security. Especifica el nivel de seguridad de un documento como un valor numérico en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.properties/documentsecurity/
---
## DocumentSecurity enum


Se usa como valor para la propiedad [Security](../builtindocumentproperties/get_security/). Especifica el nivel de seguridad de un documento como un valor numérico.

```cpp
enum class DocumentSecurity
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | No hay estados de seguridad especificados por la propiedad. |
| PasswordProtected | 1 | El documento está protegido con contraseña. (Nota: nunca se ha visto en un documento hasta ahora). |
| ReadOnlyRecommended | 2 | El documento debe abrirse en modo solo lectura si es posible, pero la configuración puede ser anulada. |
| ReadOnlyEnforced | 4 | El documento debe abrirse siempre en modo solo lectura. |
| ReadOnlyExceptAnnotations | 8 | El documento debe abrirse siempre en modo solo lectura, excepto para anotaciones. |


## Ejemplos



Muestra cómo usar las propiedades del documento para mostrar el nivel de seguridad de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::None, doc->get_BuiltInDocumentProperties()->get_Security());

// Si configuramos un documento como solo lectura, mostrará este estado usando la propiedad incorporada "Security".
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyRecommended.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyRecommended, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyRecommended.docx")->get_BuiltInDocumentProperties()->get_Security());

// Proteja contra escritura un documento y luego verifique su nivel de seguridad.
doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_FALSE(doc->get_WriteProtection()->get_IsWriteProtected());

doc->get_WriteProtection()->SetPassword(u"MyPassword");

ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));
ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyEnforced.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyEnforced, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyEnforced.docx")->get_BuiltInDocumentProperties()->get_Security());

// "Security" es una propiedad descriptiva. Podemos editar su valor manualmente.
doc = System::MakeObject<Aspose::Words::Document>();

doc->Protect(Aspose::Words::ProtectionType::AllowOnlyComments, u"MyPassword");
doc->get_BuiltInDocumentProperties()->set_Security(Aspose::Words::Properties::DocumentSecurity::ReadOnlyExceptAnnotations);
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyExceptAnnotations, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyExceptAnnotations.docx")->get_BuiltInDocumentProperties()->get_Security());
```

## Ver también

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
