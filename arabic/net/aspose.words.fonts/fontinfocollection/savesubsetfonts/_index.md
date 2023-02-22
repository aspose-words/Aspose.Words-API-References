---
title: FontInfoCollection.SaveSubsetFonts
second_title: Aspose.Words لمراجع .NET API
description: FontInfoCollection ملكية. يحدد ما إذا كان سيتم حفظ مجموعة فرعية من خطوط TrueType المضمنة مع المستند أم لا. خاطئة.
type: docs
weight: 50
url: /ar/net/aspose.words.fonts/fontinfocollection/savesubsetfonts/
---
## FontInfoCollection.SaveSubsetFonts property

يحدد ما إذا كان سيتم حفظ مجموعة فرعية من خطوط TrueType المضمنة مع المستند أم لا. **خاطئة**.

يعمل هذا الخيار فقط عندما[`EmbedTrueTypeFonts`](../embedtruetypefonts/) تم تعيين الخاصية على **حقيقي**.

```csharp
public bool SaveSubsetFonts { get; set; }
```

### ملاحظات

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


