---
title: "Método Aspose::Words::Document::Unprotect"
linktitle: "Desproteger"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Document::Unprotect. Elimina la protección del documento sin importar la contraseña en C++."
type: docs
weight: 95000
url: /es/cpp/aspose.words/document/unprotect/
---
## Document::Unprotect() method


Elimina la protección del documento sin importar la contraseña.

```cpp
void Aspose::Words::Document::Unprotect()
```

## Observaciones


Este método desprotege el documento incluso si tiene una contraseña de protección.

Tenga en cuenta que la protección del documento es diferente de la protección de escritura. La protección de escritura se especifica usando el [WriteProtection](../get_writeprotection/).

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Unprotect(const System::String\&) method


Elimina la protección del documento si se especifica una contraseña correcta.

```cpp
bool Aspose::Words::Document::Unprotect(const System::String &password)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| password | const System::String\& | La contraseña con la que desproteger el documento. |

### ReturnValue

**true** if a correct password was specified and the document was unprotected.
## Observaciones


Este método desprotege el documento solo si se especifica una contraseña correcta.

Tenga en cuenta que la protección del documento es diferente de la protección de escritura. La protección de escritura se especifica usando el [WriteProtection](../get_writeprotection/).

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
