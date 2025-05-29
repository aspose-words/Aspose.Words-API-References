---
title: DocumentBase.FontInfos
linktitle: FontInfos
articleTitle: FontInfos
second_title: Aspose.Words لـ .NET
description: يمكنك الوصول إلى خصائص الخطوط التفصيلية باستخدام ميزة FontInfos في DocumentBase، مما يعمل على تحسين تصميم مستندك وقابليته للقراءة بسهولة.
type: docs
weight: 30
url: /ar/net/aspose.words/documentbase/fontinfos/
---
## DocumentBase.FontInfos property

يوفر الوصول إلى خصائص الخطوط المستخدمة في هذه الوثيقة.

```csharp
public FontInfoCollection FontInfos { get; }
```

## ملاحظات

يتم تحميل مجموعة تعريفات الخطوط هذه كما هي من المستند. قد تكون تعريفات الخطوط اختيارية أو مفقودة أو غير كاملة في بعض المستندات.

لا تعتمد على هذه المجموعة للتأكد من استخدام خط معين في المستند. يجب عليك استخدام هذه المجموعة فقط للحصول على معلومات حول الخطوط التي يمكن استخدامها في المستند.

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

يوضح كيفية طباعة تفاصيل الخطوط الموجودة في المستند.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
//طباعة جميع الخطوط المستخدمة وغير المستخدمة في المستند.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

### أنظر أيضا

* class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* class [DocumentBase](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
