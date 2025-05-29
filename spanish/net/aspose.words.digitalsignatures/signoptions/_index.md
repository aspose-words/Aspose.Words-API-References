---
title: SignOptions Class
linktitle: SignOptions
articleTitle: SignOptions
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.DigitalSignatures.SignOptions para personalizar su proceso de firma de documentos con opciones flexibles y seguras para un flujo de trabajo mejorado.
type: docs
weight: 620
url: /es/net/aspose.words.digitalsignatures/signoptions/
---
## SignOptions class

Permite especificar opciones para la firma de documentos.

Para obtener más información, visite el[Trabajar con firmas digitales](https://docs.aspose.com/words/net/working-with-digital-signatures/) Artículo de documentación.

```csharp
public class SignOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [SignOptions](signoptions/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Comments](../../aspose.words.digitalsignatures/signoptions/comments/) { get; set; } | Especifica comentarios sobre la firma digital. El valor predeterminado es**cadena vacía**(Empty ). |
| [DecryptionPassword](../../aspose.words.digitalsignatures/signoptions/decryptionpassword/) { get; set; } | La contraseña para descifrar el documento fuente. El valor predeterminado es**cadena vacía** (Empty ). |
| [ProviderId](../../aspose.words.digitalsignatures/signoptions/providerid/) { get; set; } | Especifica el ID de clase del proveedor de firma. El valor predeterminado es**Guía vacía (todos ceros)** . |
| [SignatureLineId](../../aspose.words.digitalsignatures/signoptions/signaturelineid/) { get; set; } | Identificador de línea de firma. El valor predeterminado es**Guía vacía (todos ceros)** . |
| [SignatureLineImage](../../aspose.words.digitalsignatures/signoptions/signaturelineimage/) { get; set; } | La imagen que se mostrará en asociado[`SignatureLine`](../../aspose.words.drawing/signatureline/) . El valor predeterminado es`nulo` . |
| [SignTime](../../aspose.words.digitalsignatures/signoptions/signtime/) { get; set; } | La fecha de firma. El valor predeterminado es**hora actual** (Now) |
| [XmlDsigLevel](../../aspose.words.digitalsignatures/signoptions/xmldsiglevel/) { get; set; } | Especifica el nivel de una firma digital basada en el estándar XML-DSig. El valor predeterminado esXmlDSig . |

## Ejemplos

Muestra cómo firmar documentos digitalmente.

```csharp
// Cree un certificado X.509 desde un almacén PKCS#12, que debe contener una clave privada.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Crea un comentario y una fecha que se aplicará con nuestra nueva firma digital.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Tome un documento sin firmar del sistema de archivos local a través de un flujo de archivos,
// luego crea una copia firmada determinada por el nombre del archivo de flujo de salida.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Ver también

* espacio de nombres [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* asamblea [Aspose.Words](../../)
