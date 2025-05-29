---
title: SignOptions.DecryptionPassword
linktitle: DecryptionPassword
articleTitle: DecryptionPassword
second_title: Aspose.Words para .NET
description: Desbloquee sus documentos fácilmente con la función DecryptionPassword de SignOptions. Descifre fácilmente los archivos de origen de forma segura; la cadena predeterminada es una cadena vacía.
type: docs
weight: 30
url: /es/net/aspose.words.digitalsignatures/signoptions/decryptionpassword/
---
## SignOptions.DecryptionPassword property

La contraseña para descifrar el documento fuente. El valor predeterminado es**cadena vacía** (Empty ).

```csharp
public string DecryptionPassword { get; set; }
```

## Observaciones

Si el documento OOXML está cifrado, debe proporcionar una contraseña de descifrado para descifrar el documento de origen antes de firmarlo. Esto no es necesario para documentos en formato DOC binario.

## Ejemplos

Muestra cómo firmar un archivo de documento cifrado.

```csharp
// Cree un certificado X.509 desde un almacén PKCS#12, que debe contener una clave privada.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Crea un comentario, una fecha y una contraseña de descifrado que se aplicará con nuestra nueva firma digital.
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// Establezca un nombre de archivo de sistema local para el documento de entrada sin firmar y un nombre de archivo de salida para su nueva copia firmada digitalmente.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### Ver también

* class [SignOptions](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* asamblea [Aspose.Words](../../../)
