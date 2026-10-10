---
title: "Aspose::Words::Document::Protect método"
linktitle: "Proteger"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::Protect método. Protege el documento de cambios sin modificar la contraseña existente o asigna una contraseña aleatoria en C++."
type: docs
weight: 67000
url: /es/cpp/aspose.words/document/protect/
---
## Document::Protect(Aspose::Words::ProtectionType) method


Protege el documento de cambios sin modificar la contraseña existente o asigna una contraseña aleatoria.

```cpp
void Aspose::Words::Document::Protect(Aspose::Words::ProtectionType type)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tipo | Aspose::Words::ProtectionType | Especifica el tipo de protección del documento. |
## Observaciones


Cuando un documento está protegido, el usuario solo puede realizar cambios limitados, como añadir anotaciones, hacer revisiones o completar un formulario.

Cuando protege un documento y el documento ya tiene una contraseña de protección, la contraseña de protección existente no se cambia.

Cuando protege un documento y el documento no tiene una contraseña de protección, este método asigna una contraseña aleatoria que hace imposible desproteger el documento en Microsoft Word, pero aún puede desproteger el documento en Aspose.Words ya que no requiere una contraseña al desproteger.

## Ejemplos



Muestra cómo desactivar la protección para una sección.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Section 1. Hello world!");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

builder->Writeln(u"Section 2. Hello again!");
builder->Write(u"Please enter text here: ");
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// Aplicar protección de escritura a cada sección del documento.
doc->Protect(Aspose::Words::ProtectionType::AllowOnlyFormFields);

// Desactivar la protección de escritura para la primera sección.
doc->get_Sections()->idx_get(0)->set_ProtectedForForms(false);

// En este documento de salida, podremos editar la primera sección libremente,
// y solo podremos editar el contenido del campo de formulario en la segunda sección.
doc->Save(get_ArtifactsDir() + u"Section.Protect.docx");
```

## Ver también

* Enum [ProtectionType](../../protectiontype/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Protect(Aspose::Words::ProtectionType, const System::String\&) method


Protege el documento de cambios y opcionalmente establece una contraseña de protección.

```cpp
void Aspose::Words::Document::Protect(Aspose::Words::ProtectionType type, const System::String &password)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tipo | Aspose::Words::ProtectionType | Especifica el tipo de protección del documento. |
| password | const System::String\& | La contraseña con la que proteger el documento. Especifique **null** o una cadena vacía si desea proteger el documento sin contraseña. |
## Observaciones


Cuando un documento está protegido, el usuario solo puede realizar cambios limitados, como añadir anotaciones, hacer revisiones o completar un formulario.

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

* Enum [ProtectionType](../../protectiontype/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
