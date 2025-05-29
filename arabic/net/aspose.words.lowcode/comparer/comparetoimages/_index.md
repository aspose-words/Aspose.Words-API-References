---
title: Comparer.CompareToImages
linktitle: CompareToImages
articleTitle: CompareToImages
second_title: Aspose.Words لـ .NET
description: قم بمقارنة المستندات بسهولة باستخدام CompareToImages، وحفظ الاختلافات كصور لكل صفحة، مما يعزز الوضوح والتحليل البصري.
type: docs
weight: 30
url: /ar/net/aspose.words.lowcode/comparer/comparetoimages/
---
## CompareToImages(*string, string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#comparetoimages_1}

يقارن بين مستندين ويحفظ الاختلافات كصور. يمثل كل عنصر في المصفوفة المرتجعة صفحة واحدة من الناتج المعروض كصورة.

```csharp
public static Stream[] CompareToImages(string v1, string v2, ImageSaveOptions imageSaveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| v1 | String | الوثيقة الأصلية. |
| v2 | String | الوثيقة المعدلة. |
| imageSaveOptions | ImageSaveOptions | خيارات حفظ صورة الإخراج. |
| author | String | الأحرف الأولى من اسم المؤلف لاستخدامها في المراجعات. |
| dateTime | DateTime | التاريخ والوقت المستخدم للمراجعة. |
| compareOptions | CompareOptions | خيارات مقارنة المستندات. |

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## CompareToImages(*Stream, Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#comparetoimages}

يقارن بين مستندين ويحفظ الاختلافات كصور. يمثل كل عنصر في المصفوفة المرتجعة صفحة واحدة من الناتج المعروض كصورة.

```csharp
public static Stream[] CompareToImages(Stream v1, Stream v2, ImageSaveOptions imageSaveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| v1 | Stream | الوثيقة الأصلية. |
| v2 | Stream | الوثيقة المعدلة. |
| imageSaveOptions | ImageSaveOptions | خيارات حفظ صورة الإخراج. |
| author | String | الأحرف الأولى من اسم المؤلف لاستخدامها في المراجعات. |
| dateTime | DateTime | التاريخ والوقت المستخدم للمراجعة. |
| compareOptions | CompareOptions | خيارات مقارنة المستندات. |

## أمثلة

يوضح كيفية مقارنة المستندات وحفظ النتائج كصور.

```csharp
// هناك عدة طرق لمقارنة المستندات:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Stream[] pages = Comparer.CompareToImages(firstDoc, secondDoc, new ImageSaveOptions(SaveFormat.Png), "Author", new DateTime());

using (FileStream firstStreamIn = new FileStream(firstDoc, FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(secondDoc, FileMode.Open, FileAccess.Read))
    {
        CompareOptions compareOptions = new CompareOptions();
        compareOptions.IgnoreCaseChanges = true;
        pages = Comparer.CompareToImages(firstStreamIn, secondStreamIn, new ImageSaveOptions(SaveFormat.Png), "Author", new DateTime(), compareOptions);
    }
}
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
