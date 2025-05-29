---
title: FontInfoCollection.SaveSubsetFonts
linktitle: SaveSubsetFonts
articleTitle: SaveSubsetFonts
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية SaveSubsetFonts في FontInfoCollection، وتحكم في مجموعات الخطوط TrueType المضمنة في مستنداتك لتحسين حجم الملف والأداء.
type: docs
weight: 50
url: /ar/net/aspose.words.fonts/fontinfocollection/savesubsetfonts/
---
## FontInfoCollection.SaveSubsetFonts property

يحدد ما إذا كان سيتم حفظ مجموعة فرعية من خطوط TrueType المضمنة مع المستند أم لا. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع`.

يعمل هذا الخيار فقط عندما[`EmbedTrueTypeFonts`](../embedtruetypefonts/) تم تعيين الخاصية إلى`حقيقي`.

```csharp
public bool SaveSubsetFonts { get; set; }
```

## ملاحظات

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
