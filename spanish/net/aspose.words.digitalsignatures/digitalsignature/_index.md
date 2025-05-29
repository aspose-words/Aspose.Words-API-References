---
title: DigitalSignature Class
linktitle: DigitalSignature
articleTitle: DigitalSignature
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.DigitalSignatures.DigitalSignature para la firma y verificación segura de documentos. ¡Mejore la seguridad de sus documentos sin esfuerzo!
type: docs
weight: 580
url: /es/net/aspose.words.digitalsignatures/digitalsignature/
---
## DigitalSignature class

Representa una firma digital en un documento y el resultado de su verificación.

Para obtener más información, visite el[Trabajar con firmas digitales](https://docs.aspose.com/words/net/working-with-digital-signatures/) Artículo de documentación.

```csharp
public class DigitalSignature
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CertificateHolder](../../aspose.words.digitalsignatures/digitalsignature/certificateholder/) { get; } | Devuelve el objeto titular del certificado que contiene el certificado que se utilizó para firmar el documento. |
| [Comments](../../aspose.words.digitalsignatures/digitalsignature/comments/) { get; } | Obtiene el comentario del propósito de la firma. |
| [IssuerName](../../aspose.words.digitalsignatures/digitalsignature/issuername/) { get; } | Devuelve el nombre distinguido del sujeto del emisor del certificado. |
| [IsValid](../../aspose.words.digitalsignatures/digitalsignature/isvalid/) { get; } | Devuelve`verdadero` si esta firma digital es válida y el documento no ha sido alterado. |
| [SignatureType](../../aspose.words.digitalsignatures/digitalsignature/signaturetype/) { get; } | Obtiene el tipo de firma digital. |
| [SignatureValue](../../aspose.words.digitalsignatures/digitalsignature/signaturevalue/) { get; } | Obtiene una matriz de bytes que representan un valor de firma. |
| [SignTime](../../aspose.words.digitalsignatures/digitalsignature/signtime/) { get; } | Obtiene la hora en que se firmó el documento. |
| [SubjectName](../../aspose.words.digitalsignatures/digitalsignature/subjectname/) { get; } | Devuelve el nombre distinguido del sujeto del certificado que se utilizó para firmar el documento. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [ToString](../../aspose.words.digitalsignatures/digitalsignature/tostring/)() | Devuelve una cadena fácil de usar que muestra el valor de este objeto. |

## Ejemplos

Muestra cómo validar y mostrar información sobre cada firma en un documento.

```csharp
Document doc = new Document(MyDir + "Digitally signed.docx");

foreach (DigitalSignature signature in doc.DigitalSignatures)
{
    Console.WriteLine($"{(signature.IsValid ? "Valid" : "Invalid")} signature: ");
    Console.WriteLine($"\tReason:\t{signature.Comments}");
    Console.WriteLine($"\tType:\t{signature.SignatureType}");
    Console.WriteLine($"\tSign time:\t{signature.SignTime}");
    Console.WriteLine($"\tSubject name:\t{signature.CertificateHolder.Certificate.SubjectName}");
    Console.WriteLine($"\tIssuer name:\t{signature.CertificateHolder.Certificate.IssuerName.Name}");
    Console.WriteLine();
}
```

### Ver también

* espacio de nombres [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* asamblea [Aspose.Words](../../)
