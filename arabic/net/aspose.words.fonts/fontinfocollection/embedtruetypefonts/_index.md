---
title: FontInfoCollection.EmbedTrueTypeFonts
linktitle: EmbedTrueTypeFonts
articleTitle: EmbedTrueTypeFonts
second_title: Aspose.Words لـ .NET
description: تعرّف على كيفية تحسين خاصية EmbedTrueTypeFonts في FontInfoCollection لجودة المستند من خلال السماح بتضمين خطوط TrueType. القيمة الافتراضية هي False.
type: docs
weight: 30
url: /ar/net/aspose.words.fonts/fontinfocollection/embedtruetypefonts/
---
## FontInfoCollection.EmbedTrueTypeFonts property

يحدد ما إذا كان سيتم تضمين خطوط TrueType في مستند عند حفظه أم لا. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` .

```csharp
public bool EmbedTrueTypeFonts { get; set; }
```

## ملاحظات

يتيح تضمين خطوط TrueType للآخرين عرض المستند باستخدام نفس الخطوط التي تم استخدامها لإنشائه، ولكن قد يؤدي ذلك إلى زيادة حجم المستند بشكل كبير.

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
