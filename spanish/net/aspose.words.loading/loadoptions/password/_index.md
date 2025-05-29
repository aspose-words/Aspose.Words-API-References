---
title: LoadOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words para .NET
description: Administre sus documentos cifrados fácilmente con la propiedad LoadOptions Password. Configure o recupere su contraseña de forma segura para un acceso sin problemas.
type: docs
weight: 110
url: /es/net/aspose.words.loading/loadoptions/password/
---
## LoadOptions.Password property

Obtiene o establece la contraseña para abrir un documento cifrado. Puede ser`nulo` o cadena vacía. El valor predeterminado es`nulo` .

```csharp
public string Password { get; set; }
```

## Observaciones

Necesita saber la contraseña para abrir un documento cifrado. Si el documento no está cifrado, configúrelo como`nulo` o cadena vacía.

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

* class [LoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
