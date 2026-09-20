---
title: "Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword método"
linktitle: "get_DecryptionPassword"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword method. La contraseña para descifrar el documento fuente. El valor predeterminado es una cadena vacía en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.digitalsignatures/signoptions/get_decryptionpassword/
---
## SignOptions::get_DecryptionPassword method


La contraseña para descifrar el documento fuente. El valor predeterminado es **empty string**.

```cpp
System::String Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword() const
```


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

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
