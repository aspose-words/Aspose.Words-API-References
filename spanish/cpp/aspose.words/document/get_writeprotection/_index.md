---
title: "Método Aspose::Words::Document::get_WriteProtection"
linktitle: "get_WriteProtection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Document::get_WriteProtection. Proporciona acceso a las opciones de protección contra escritura del documento en C++."
type: docs
weight: 61000
url: /es/cpp/aspose.words/document/get_writeprotection/
---
## Document::get_WriteProtection method


Proporciona acceso a las opciones de protección contra escritura del documento.

```cpp
System::SharedPtr<Aspose::Words::Settings::WriteProtection> Aspose::Words::Document::get_WriteProtection()
```


## Ejemplos



Muestra cómo proteger un documento con una contraseña.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This document is protected.");

// Introduzca una contraseña de hasta 15 caracteres de longitud y luego verifique el estado de protección del documento.
doc->get_WriteProtection()->SetPassword(u"MyPassword");
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());
ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));

// La protección no impide que el documento sea editado programáticamente, ni cifra el contenido.
doc->Save(get_ArtifactsDir() + u"Document.WriteProtection.docx");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.WriteProtection.docx");

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u"Writing text in a protected document.");

ASSERT_EQ(System::String(u"Hello world! This document is protected.") + u"\rWriting text in a protected document.", doc->GetText().Trim());
```

## Ver también

* Class [WriteProtection](../../../aspose.words.settings/writeprotection/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
