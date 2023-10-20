---
title: FontInfoCollection Class
linktitle: FontInfoCollection
articleTitle: FontInfoCollection
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fonts.FontInfoCollection فصل. يمثل مجموعة من الخطوط المستخدمة في المستند في C#.
type: docs
weight: 2930
url: /ar/net/aspose.words.fonts/fontinfocollection/
---
## FontInfoCollection class

يمثل مجموعة من الخطوط المستخدمة في المستند.

لمعرفة المزيد، قم بزيارة[العمل مع الخطوط](https://docs.aspose.com/words/net/working-with-fonts/) مقالة توثيقية.

```csharp
public class FontInfoCollection : IEnumerable<FontInfo>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.fonts/fontinfocollection/count/) { get; } | الحصول على عدد العناصر الموجودة في المجموعة. |
| [EmbedSystemFonts](../../aspose.words.fonts/fontinfocollection/embedsystemfonts/) { get; set; } | يحدد ما إذا كان سيتم تضمين خطوط النظام في المستند أم لا. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع`. |
| [EmbedTrueTypeFonts](../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) { get; set; } | يحدد ما إذا كان سيتم تضمين خطوط TrueType في مستند عند حفظه أم لا. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` . |
| [Item](../../aspose.words.fonts/fontinfocollection/item/) { get; } | الحصول على خط بالاسم المحدد. (2 indexers) |
| [SaveSubsetFonts](../../aspose.words.fonts/fontinfocollection/savesubsetfonts/) { get; set; } | يحدد ما إذا كان سيتم حفظ مجموعة فرعية من خطوط TrueType المضمنة مع المستند أم لا. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع`. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Contains](../../aspose.words.fonts/fontinfocollection/contains/)(*string*) | يحدد ما إذا كانت المجموعة تحتوي على خط بالاسم المحدد. |
| [GetEnumerator](../../aspose.words.fonts/fontinfocollection/getenumerator/)() | إرجاع كائن العداد الذي يمكن استخدامه للتكرار على كافة العناصر الموجودة في المجموعة. |

## ملاحظات

العناصر هي[`FontInfo`](../fontinfo/) أشياء.

لا تقم بإنشاء مثيلات هذه الفئة مباشرة. استخدم[`FontInfos`](../../aspose.words/documentbase/fontinfos/) خاصية الوصول إلى مجموعة الخطوط المحددة في المستند.

## أمثلة

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

* class [FontInfo](../fontinfo/)
* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)
