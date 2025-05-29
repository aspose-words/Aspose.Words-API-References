---
title: XmlDsigLevel Enum
linktitle: XmlDsigLevel
articleTitle: XmlDsigLevel
second_title: Aspose.Words para .NET
description: Explore la enumeración Aspose.Words.DigitalSignatures.XmlDsigLevel para mejorar sus firmas digitales con los estándares XMLDSig para una integridad de documentos segura y confiable.
type: docs
weight: 630
url: /es/net/aspose.words.digitalsignatures/xmldsiglevel/
---
## XmlDsigLevel enumeration

Especifica el nivel de una firma digital basada en el estándar XML-DSig.

```csharp
public enum XmlDsigLevel
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| XmlDSig | `0` | Especifica el nivel de firma XML-DSig. |
| XAdEsEpes | `1` | Especifica el nivel de firma XAdES-EPES. |

## Ejemplos

Muestra cómo firmar documentos según el estándar XML-DSig.

```csharp
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
SignOptions signOptions = new SignOptions { XmlDsigLevel = XmlDsigLevel.XAdEsEpes };

string inputFileName = MyDir + "Document.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.XmlDsig.docx";
DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### Ver también

* espacio de nombres [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* asamblea [Aspose.Words](../../)
