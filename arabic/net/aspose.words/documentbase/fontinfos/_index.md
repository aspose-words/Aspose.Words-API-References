---
title: DocumentBase.FontInfos
second_title: Aspose.Words لمراجع .NET API
description: DocumentBase ملكية. يوفر الوصول إلى خصائص الخطوط المستخدمة في هذا المستند.
type: docs
weight: 30
url: /ar/net/aspose.words/documentbase/fontinfos/
---
## DocumentBase.FontInfos property

يوفر الوصول إلى خصائص الخطوط المستخدمة في هذا المستند.

```csharp
public FontInfoCollection FontInfos { get; }
```

### ملاحظات

يتم تحميل مجموعة تعريفات الخطوط هذه كما هي من المستند. قد تكون تعريفات الخطوط اختيارية أو مفقودة أو غير كاملة في بعض المستندات.

لا تعتمد على هذه المجموعة للتأكد من استخدام خط معين في الوثيقة. يجب عليك استخدام هذه المجموعة فقط للحصول على معلومات حول الخطوط التي يمكن استخدامها في الوثيقة.

### أمثلة

يوضح كيفية طباعة تفاصيل الخطوط الموجودة في المستند.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// اطبع جميع الخطوط المستخدمة وغير المستخدمة في المستند.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

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

* class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* class [DocumentBase](../)
* مساحة الاسم [Aspose.Words](../../documentbase/)
* المجسم [Aspose.Words](../../../)


