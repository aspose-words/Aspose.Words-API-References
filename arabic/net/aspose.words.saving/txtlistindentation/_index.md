---
title: TxtListIndentation Class
linktitle: TxtListIndentation
articleTitle: TxtListIndentation
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Saving.TxtListIndentation لتخصيص مستويات المسافة البادئة للقوائم لتصدير نصوص سلس. حسّن تنسيق مستندك!
type: docs
weight: 6450
url: /ar/net/aspose.words.saving/txtlistindentation/
---
## TxtListIndentation class

يحدد كيفية تحديد مستويات القائمة عند تصدير المستند إلىText تنسيق.

لمعرفة المزيد، قم بزيارة[حفظ مستند](https://docs.aspose.com/words/net/save-a-document/) مقالة توثيقية.

```csharp
public class TxtListIndentation
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [TxtListIndentation](txtlistindentation/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Character](../../aspose.words.saving/txtlistindentation/character/) { get; set; } | يحصل على أو يحدد الحرف الذي سيتم استخدامه لتعيين مستويات القائمة. القيمة الافتراضية هي '\0'، وهذا يعني أنه لا يوجد مسافة بادئة. |
| [Count](../../aspose.words.saving/txtlistindentation/count/) { get; set; } | يحصل على أو يحدد عدد[`Character`](./character/)لاستخدامه كمسافة بادئة لكل مستوى قائمة. القيمة الافتراضية هي 0، وهذا يعني عدم وجود مسافة بادئة. |

## أمثلة

يوضح كيفية تكوين المسافة البادئة للقائمة عند حفظ مستند في نص عادي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء قائمة تحتوي على ثلاثة مستويات من المسافة البادئة.
builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent(); 
builder.Write("Item 3");

// قم بإنشاء كائن "TxtSaveOptions"، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية حفظ المستند إلى نص عادي.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// قم بتعيين خاصية "الحرف" لتعيين حرف للاستخدام
// للحشو الذي يحاكي مسافة البادئة للقائمة في النص العادي.
txtSaveOptions.ListIndentation.Character = ' ';

// اضبط خاصية "Count" لتحديد عدد المرات
//لوضع حرف الحشو لكل مستوى مسافة بادئة للقائمة.
txtSaveOptions.ListIndentation.Count = 3;

doc.Save(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt");
string newLine= Environment.NewLine;

Assert.AreEqual($"1. Item 1{newLine}" +
                $"   a. Item 2{newLine}" +
                $"      i. Item 3{newLine}", docText);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
