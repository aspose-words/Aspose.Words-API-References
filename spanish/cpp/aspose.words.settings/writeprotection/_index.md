---
title: "Clase Aspose::Words::Settings::WriteProtection"
linktitle: "WriteProtection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Settings::WriteProtection. Especifica la configuración de protección contra escritura para un documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.settings/writeprotection/
---
## WriteProtection class


Especifica la configuración de protección contra escritura para un documento. Para obtener más información, visite el artículo de documentación [Protect or Encrypt a Document](https://docs.aspose.com/words/cpp/protect-or-encrypt-a-document/).

```cpp
class WriteProtection : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_IsWriteProtected](./get_iswriteprotected/)() | Devuelve **true** cuando se establece una contraseña de protección contra escritura. |
| [get_ReadOnlyRecommended](./get_readonlyrecommended/)() const | Especifica si el autor del documento ha recomendado que el documento se abra como solo lectura. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ReadOnlyRecommended](./set_readonlyrecommended/)(bool) | Método setter para [Aspose::Words::Settings::WriteProtection::get_ReadOnlyRecommended](./get_readonlyrecommended/). |
| [SetPassword](./setpassword/)(const System::String\&) | Establece la contraseña de protección contra escritura para el documento. |
| static [Type](./type/)() |  |
| [ValidatePassword](./validatepassword/)(const System::String\&) | Devuelve **true** si la contraseña especificada es la misma que la contraseña de protección contra escritura con la que se protegió el documento. Si el documento no está protegido contra escritura con contraseña, devuelve **false**. |
## Observaciones


La protección contra escritura especifica si el autor ha recomendado que el documento se abra como solo lectura y/o requiera una contraseña para modificar el documento.

La protección de escritura es diferente de la protección de documento. La protección de escritura se especifica en Microsoft Word en las opciones del cuadro de diálogo Guardar como.

No crea instancias de esta clase directamente. Accede a la configuración de protección de documento a través de la propiedad [WriteProtection](../../aspose.words/document/get_writeprotection/).

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

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
