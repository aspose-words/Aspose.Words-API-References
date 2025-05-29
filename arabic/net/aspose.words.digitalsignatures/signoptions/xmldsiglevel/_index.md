---
title: SignOptions.XmlDsigLevel
linktitle: XmlDsigLevel
articleTitle: XmlDsigLevel
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية XmlDsigLevel في SignOptions، التي تُحدد قوة التوقيع الرقمي وفقًا لمعايير XMLDSig. اضمن توقيعات آمنة وموثوقة!
type: docs
weight: 80
url: /ar/net/aspose.words.digitalsignatures/signoptions/xmldsiglevel/
---
## SignOptions.XmlDsigLevel property

يحدد مستوى التوقيع الرقمي استنادًا إلى معيار XML-DSig. القيمة الافتراضية هيXmlDSig .

```csharp
public XmlDsigLevel XmlDsigLevel { get; set; }
```

## ملاحظات

يمكن إنشاء مستويات مختلفة من توقيعات XAdES بدءًا من Office 2010.

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

* enum [XmlDsigLevel](../../xmldsiglevel/)
* class [SignOptions](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../../)
