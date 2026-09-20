---
title: "Aspose::Words::Document::get_ProtectionType método"
linktitle: "get_ProtectionType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::get_ProtectionType método. Obtiene el tipo de protección de documento actualmente activo en C++."
type: docs
weight: 44000
url: /es/cpp/aspose.words/document/get_protectiontype/
---
## Document::get_ProtectionType method


Obtiene el tipo de protección de documento actualmente activo.

```cpp
Aspose::Words::ProtectionType Aspose::Words::Document::get_ProtectionType()
```

## Observaciones


Esta propiedad permite recuperar el tipo de protección de documento establecido actualmente. Para cambiar el tipo de protección de documento use los métodos [Protect()](../) y [Unprotect](../unprotect/).

Cuando un documento está protegido, el usuario solo puede realizar cambios limitados, como añadir anotaciones, hacer revisiones o completar un formulario.

Tenga en cuenta que la protección de documento es diferente de la protección de escritura. La protección de escritura se especifica usando el [WriteProtection](../get_writeprotection/)

## Ejemplos



Muestra cómo proteger y desproteger un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"password");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

// Si abrimos este documento con Microsoft Word con la intención de editarlo,
// necesitaremos aplicar la contraseña para pasar la protección.
doc->Save(get_ArtifactsDir() + u"Document.Protect.docx");

// Tenga en cuenta que la protección solo se aplica a los usuarios de Microsoft Word que abren nuestro documento.
// No hemos cifrado el documento de ninguna manera, y no necesitamos la contraseña para abrirlo y editarlo programáticamente.
auto protectedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.Protect.docx");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, protectedDoc->get_ProtectionType());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(protectedDoc);
builder->Writeln(u"Text added to a protected document.");

// Hay dos formas de eliminar la protección de un documento.
// 1 - Sin contraseña:
doc->Unprotect();

ASSERT_EQ(Aspose::Words::ProtectionType::NoProtection, doc->get_ProtectionType());

doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"NewPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

doc->Unprotect(u"WrongPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

// 2 - Con la contraseña correcta:
doc->Unprotect(u"NewPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::NoProtection, doc->get_ProtectionType());
```

## Ver también

* Enum [ProtectionType](../../protectiontype/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
