---
title: "Aspose::Words::Settings::WriteProtection::get_IsWriteProtected método"
linktitle: "get_IsWriteProtected"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Settings::WriteProtection::get_IsWriteProtected método. Devuelve true cuando se ha establecido una contraseña de protección de escritura en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.settings/writeprotection/get_iswriteprotected/
---
## WriteProtection::get_IsWriteProtected method


Devuelve **true** cuando se establece una contraseña de protección contra escritura.

```cpp
bool Aspose::Words::Settings::WriteProtection::get_IsWriteProtected()
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

* Class [WriteProtection](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
