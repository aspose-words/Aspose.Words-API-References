---
title: FontInfoCollection.EmbedTrueTypeFonts
second_title: Aspose.Words لمراجع .NET API
description: FontInfoCollection ملكية. يحدد ما إذا كان سيتم تضمين خطوط TrueType في مستند أم لا عند حفظه. القيمة الافتراضية لهذه الخاصية هي خاطئة .
type: docs
weight: 30
url: /ar/net/aspose.words.fonts/fontinfocollection/embedtruetypefonts/
---
## FontInfoCollection.EmbedTrueTypeFonts property

يحدد ما إذا كان سيتم تضمين خطوط TrueType في مستند أم لا عند حفظه. القيمة الافتراضية لهذه الخاصية هي **خاطئة** .

```csharp
public bool EmbedTrueTypeFonts { get; set; }
```

### ملاحظات

يتيح دمج خطوط TrueType للآخرين عرض المستند بنفس الخطوط التي تم استخدامها لإنشائه ، ولكن قد يؤدي إلى زيادة حجم المستند بشكل كبير.

يعمل هذا الخيار مع تنسيقات DOC و DOCX و RTF فقط.

### أمثلة

يوضح كيفية حفظ مستند بخطوط TrueType المضمنة.

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


