---
title: SignOptions.XmlDsigLevel
linktitle: XmlDsigLevel
articleTitle: XmlDsigLevel
second_title: Aspose.Words per .NET
description: Scopri la proprietà XmlDsigLevel in SignOptions, che definisce la forza della firma digitale secondo gli standard XMLDSig. Garantisci firme sicure e affidabili!
type: docs
weight: 80
url: /it/net/aspose.words.digitalsignatures/signoptions/xmldsiglevel/
---
## SignOptions.XmlDsigLevel property

Specifica il livello di una firma digitale basata sullo standard XML-DSig. Il valore predefinito èXmlDSig .

```csharp
public XmlDsigLevel XmlDsigLevel { get; set; }
```

## Osservazioni

A partire da Office 2010 è possibile creare diversi livelli di firme XAdES.

## Esempi

Mostra come firmare documenti basati sullo standard XML-DSig.

```csharp
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
SignOptions signOptions = new SignOptions { XmlDsigLevel = XmlDsigLevel.XAdEsEpes };

string inputFileName = MyDir + "Document.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.XmlDsig.docx";
DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### Guarda anche

* enum [XmlDsigLevel](../../xmldsiglevel/)
* class [SignOptions](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../../)
