---
title: "Método Aspose::Words::Loading::LoadOptions::get_Password"
linktitle: "get_Password"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Loading::LoadOptions::get_Password. Obtiene o establece la contraseña para abrir un documento cifrado. Puede ser null o una cadena vacía. El valor predeterminado es null en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words.loading/loadoptions/get_password/
---
## LoadOptions::get_Password method


Obtiene o establece la contraseña para abrir un documento cifrado. Puede ser **null** o una cadena vacía. El valor predeterminado es **null**.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_Password() const
```

## Observaciones


Necesitas conocer la contraseña para abrir un documento cifrado. Si el documento no está cifrado, establece esto a **null** o una cadena vacía.

## Ejemplos



Muestra cómo firmar un archivo de documento cifrado.
```cpp
// Crea un certificado X.509 a partir de un almacén PKCS#12, que debe contener una clave privada.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Crea un comentario, una fecha y una contraseña de descifrado que se aplicarán con nuestra nueva firma digital.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

// Establezca un nombre de archivo del sistema local para el documento de entrada sin firmar, y un nombre de archivo de salida para su nueva copia firmada digitalmente.
System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.DecryptionPassword.docx";

Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## Ver también

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
