---
title: FontInfoCollection.EmbedTrueTypeFonts
second_title: Aspose.Words لمراجع .NET API
description: FontInfoCollection ملكية. يحدد ما إذا كان سيتم تضمين خطوط TrueType في مستند عند حفظه أم لا. القيمة الافتراضية لهذه الخاصية هيخطأ شنيع .
type: docs
weight: 30
url: /ar/net/aspose.words.fonts/fontinfocollection/embedtruetypefonts/
---
## FontInfoCollection.EmbedTrueTypeFonts property

يحدد ما إذا كان سيتم تضمين خطوط TrueType في مستند عند حفظه أم لا. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` .

```csharp
public bool EmbedTrueTypeFonts { get; set; }
```

### ملاحظات

يتيح تضمين خطوط TrueType للآخرين إمكانية عرض المستند بنفس الخطوط التي تم استخدامها لإنشائه، ولكنه قد يؤدي إلى زيادة حجم المستند بشكل كبير.

يعمل هذا الخيار مع تنسيقات DOC وDOCX وRTF فقط.

### أمثلة

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
* مساحة الاسم [Aspose.Words.Fonts](../../fontinfocollection/)
* المجسم [Aspose.Words](../../../)


