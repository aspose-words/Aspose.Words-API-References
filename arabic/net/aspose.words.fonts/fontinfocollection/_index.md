---
title: FontInfoCollection Class
linktitle: FontInfoCollection
articleTitle: FontInfoCollection
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fonts.FontInfoCollection، الحل الأمثل لإدارة خطوط المستندات بكفاءة وتعزيز المظهر المرئي لمستندك.
type: docs
weight: 3360
url: /ar/net/aspose.words.fonts/fontinfocollection/
---
## FontInfoCollection class

يمثل مجموعة الخطوط المستخدمة في المستند.

لمعرفة المزيد، قم بزيارة[العمل مع الخطوط](https://docs.aspose.com/words/net/working-with-fonts/) مقالة توثيقية.

```csharp
public class FontInfoCollection : IEnumerable<FontInfo>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.fonts/fontinfocollection/count/) { get; } | يحصل على عدد العناصر الموجودة في المجموعة. |
| [EmbedSystemFonts](../../aspose.words.fonts/fontinfocollection/embedsystemfonts/) { get; set; } | يحدد ما إذا كان سيتم تضمين خطوط النظام في المستند أم لا. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع`. |
| [EmbedTrueTypeFonts](../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) { get; set; } | يحدد ما إذا كان سيتم تضمين خطوط TrueType في مستند عند حفظه أم لا. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` . |
| [Item](../../aspose.words.fonts/fontinfocollection/item/) { get; } | يحصل على خط بالاسم المحدد. (2 indexers) |
| [SaveSubsetFonts](../../aspose.words.fonts/fontinfocollection/savesubsetfonts/) { get; set; } | يحدد ما إذا كان سيتم حفظ مجموعة فرعية من خطوط TrueType المضمنة مع المستند أم لا. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع`. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Contains](../../aspose.words.fonts/fontinfocollection/contains/)(*string*) | يحدد ما إذا كانت المجموعة تحتوي على خط يحمل الاسم المحدد. |
| [GetEnumerator](../../aspose.words.fonts/fontinfocollection/getenumerator/)() | يعيد كائن عداد يمكن استخدامه للتكرار على جميع العناصر في المجموعة. |

## ملاحظات

العناصر هي[`FontInfo`](../fontinfo/) أشياء.

لا يمكنك إنشاء مثيلات لهذه الفئة بشكل مباشر. استخدم[`FontInfos`](../../aspose.words/documentbase/fontinfos/) الخاصية للوصول إلى مجموعة الخطوط المحددة في المستند.

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

* class [FontInfo](../fontinfo/)
* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)
