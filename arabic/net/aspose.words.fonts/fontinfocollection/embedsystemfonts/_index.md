---
title: FontInfoCollection.EmbedSystemFonts
linktitle: EmbedSystemFonts
articleTitle: EmbedSystemFonts
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية FontInfoCollection EmbedSystemFonts مستنداتك بتضمين خطوط النظام. تعرّف على قيمتها الافتراضية وفوائدها!
type: docs
weight: 20
url: /ar/net/aspose.words.fonts/fontinfocollection/embedsystemfonts/
---
## FontInfoCollection.EmbedSystemFonts property

يحدد ما إذا كان سيتم تضمين خطوط النظام في المستند أم لا. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع`.

يعمل هذا الخيار فقط عندما[`EmbedTrueTypeFonts`](../embedtruetypefonts/) تم تعيين الخيار على`حقيقي`.

```csharp
public bool EmbedSystemFonts { get; set; }
```

## ملاحظات

تعيين هذه الخاصية إلى`حقيقي` يُفيد هذا إذا كان المستخدم يستخدم نظامًا شرق آسيويًا ويرغب في إنشاء مستند يمكن قراءته من قِبل الآخرين الذين لا يملكون خطوطًا لتلك اللغة على نظامهم. على سبيل المثال، يمكن لمستخدم يستخدم نظامًا يابانيًا تضمين خطوط تلك اللغة في مستند ليصبح المستند الياباني قابلًا للقراءة على جميع الأنظمة.

يعمل هذا الخيار مع تنسيقات DOC وDOCX وRTF فقط.

## أمثلة

يوضح كيفية حفظ مستند يحتوي على خطوط TrueType المضمنة.

```csharp
Document doc = new Document(MyDir + "Document.docx");

FontInfoCollection fontInfos = doc.FontInfos;
fontInfos.EmbedTrueTypeFonts = embedAllFonts;
fontInfos.EmbedSystemFonts = embedAllFonts;
fontInfos.SaveSubsetFonts = embedAllFonts;

doc.Save(ArtifactsDir + "Font.FontInfoCollection.docx");
```

### أنظر أيضا

* class [FontInfoCollection](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
