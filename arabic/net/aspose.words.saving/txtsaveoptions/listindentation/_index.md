---
title: TxtSaveOptions.ListIndentation
linktitle: ListIndentation
articleTitle: ListIndentation
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية TxtSaveOptions ListIndentation، التي تُخصّص المسافة البادئة للقائمة لتحسين قابلية القراءة. تحكّم بالأحرف والمستويات بسهولة!
type: docs
weight: 30
url: /ar/net/aspose.words.saving/txtsaveoptions/listindentation/
---
## TxtSaveOptions.ListIndentation property

يحصل على[`TxtListIndentation`](../../txtlistindentation/)كائن يحدد عدد الأحرف التي سيتم استخدامها لتحديد مسافة بادئة لمستويات القائمة. بشكل افتراضي، يكون عدد الأحرف '\0' صفرًا، وهذا يعني عدم وجود مسافة بادئة.

```csharp
public TxtListIndentation ListIndentation { get; }
```

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

* class [TxtListIndentation](../../txtlistindentation/)
* class [TxtSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
