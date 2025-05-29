---
title: SignOptions.XmlDsigLevel
linktitle: XmlDsigLevel
articleTitle: XmlDsigLevel
second_title: Aspose.Words para .NET
description: Descubra la propiedad XmlDsigLevel en SignOptions, que define la solidez de la firma digital según los estándares XMLDSig. ¡Asegure firmas seguras y confiables!
type: docs
weight: 80
url: /es/net/aspose.words.digitalsignatures/signoptions/xmldsiglevel/
---
## SignOptions.XmlDsigLevel property

Especifica el nivel de una firma digital basada en el estándar XML-DSig. El valor predeterminado esXmlDSig .

```csharp
public XmlDsigLevel XmlDsigLevel { get; set; }
```

## Observaciones

Se pueden crear diferentes niveles de firmas XAdES a partir de Office 2010.

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

* enum [XmlDsigLevel](../../xmldsiglevel/)
* class [SignOptions](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* asamblea [Aspose.Words](../../../)
