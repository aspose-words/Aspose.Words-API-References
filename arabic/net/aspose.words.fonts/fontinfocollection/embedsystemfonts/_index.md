---
title: FontInfoCollection.EmbedSystemFonts
linktitle: EmbedSystemFonts
articleTitle: EmbedSystemFonts
second_title: Aspose.Words لـ .NET
description: FontInfoCollection EmbedSystemFonts ملكية. يحدد ما إذا كان سيتم تضمين خطوط النظام في المستند أم لا. القيمة الافتراضية لهذه الخاصية هيخطأ شنيع في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fonts/fontinfocollection/embedsystemfonts/
---
## FontInfoCollection.EmbedSystemFonts property

يحدد ما إذا كان سيتم تضمين خطوط النظام في المستند أم لا. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع`.

هذا الخيار يعمل فقط عندما[`EmbedTrueTypeFonts`](../embedtruetypefonts/) تم ضبط الخيار على`حقيقي`.

```csharp
public bool EmbedSystemFonts { get; set; }
```

## ملاحظات

تعيين هذه الخاصية على`حقيقي`يكون مفيدًا إذا كان المستخدم يستخدم نظامًا شرق آسيويًا ويريد إنشاء مستند يمكن قراءته بواسطة الآخرين الذين ليس لديهم خطوط لهذه اللغة على نظامهم. على سبيل المثال، يمكن لمستخدم النظام الياباني اختيار تضمين الخطوط في مستند بحيث يكون المستند الياباني قابلاً للقراءة على جميع الأنظمة.

يعمل هذا الخيار مع تنسيقات DOC وDOCX وRTF فقط.

## أمثلة

يوضح كيفية حفظ مستند باستخدام خطوط TrueType المضمنة.

```csharp
Document doc = new Document(MyDir + "Document.docx");

FontInfoCollection fontInfos = doc.FontInfos;
fontInfos.EmbedTrueTypeFonts = embedAllFonts;
fontInfos.EmbedSystemFonts = embedAllFonts;
fontInfos.SaveSubsetFonts = embedAllFonts;

doc.Save(ArtifactsDir + "Font.FontInfoCollection.docx");

if (embedAllFonts)
    Assert.That(25000, Is.LessThan(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
else
    Assert.That(15000, Is.AtLeast(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
```

### أنظر أيضا

* class [FontInfoCollection](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
