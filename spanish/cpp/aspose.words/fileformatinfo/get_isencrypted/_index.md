---
title: "Aspose::Words::FileFormatInfo::get_IsEncrypted método"
linktitle: "get_IsEncrypted"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::FileFormatInfo::get_IsEncrypted método. Devuelve true si el documento está encriptado y requiere una contraseña para abrirse en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/fileformatinfo/get_isencrypted/
---
## FileFormatInfo::get_IsEncrypted method


Devuelve **true** si el documento está encriptado y requiere una contraseña para abrirse.

```cpp
bool Aspose::Words::FileFormatInfo::get_IsEncrypted() const
```

## Observaciones


Esta propiedad existe para ayudarle a separar los documentos que están encriptados de los que no lo están. Si intenta cargar un documento encriptado usando Aspose.Words sin proporcionar una contraseña, se lanzará una excepción. Puede usar esta propiedad para detectar si un documento requiere una contraseña y tomar alguna acción antes de cargarlo, por ejemplo, solicitar al usuario una contraseña.

## Ejemplos



Muestra cómo usar la clase [FileFormatUtil](../../fileformatutil/) para detectar el formato del documento y la encriptación.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Configure un objeto SaveOptions para encriptar el documento
// con una contraseña al guardarlo, y luego guarde el documento.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(Aspose::Words::SaveFormat::Odt);
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt", saveOptions);

// Verifique el tipo de archivo de nuestro documento y su estado de encriptación.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt");

ASSERT_EQ(u".odt", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_TRUE(info->get_IsEncrypted());
```

## Ver también

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
