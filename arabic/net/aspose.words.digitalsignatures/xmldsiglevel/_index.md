---
title: XmlDsigLevel Enum
linktitle: XmlDsigLevel
articleTitle: XmlDsigLevel
second_title: Aspose.Words لـ .NET
description: استكشف Aspose.Words.DigitalSignatures.XmlDsigLevel enum لتعزيز توقيعاتك الرقمية بمعايير XMLDSig لضمان سلامة المستندات بشكل آمن وموثوق.
type: docs
weight: 630
url: /ar/net/aspose.words.digitalsignatures/xmldsiglevel/
---
## XmlDsigLevel enumeration

يحدد مستوى التوقيع الرقمي استنادًا إلى معيار XML-DSig.

```csharp
public enum XmlDsigLevel
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| XmlDSig | `0` | يحدد مستوى توقيع XML-DSig. |
| XAdEsEpes | `1` | يحدد مستوى توقيع XAdES-EPES. |

## أمثلة

يوضح كيفية توقيع المستندات استنادًا إلى معيار XML-DSig.

```csharp
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
SignOptions signOptions = new SignOptions { XmlDsigLevel = XmlDsigLevel.XAdEsEpes };

string inputFileName = MyDir + "Document.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.XmlDsig.docx";
DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../)
