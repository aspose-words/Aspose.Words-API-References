---
title: TxtListIndentation.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words لـ .NET
description: TxtListIndentation Count ملكية. الحصول على العدد أو تعيينهCharacter لاستخدامها كمسافة بادئة لكل مستوى قائمة. القيمة الافتراضية هي 0 وهذا يعني عدم وجود مسافة بادئة في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/txtlistindentation/count/
---
## TxtListIndentation.Count property

الحصول على العدد أو تعيينه[`Character`](../character/) لاستخدامها كمسافة بادئة لكل مستوى قائمة. القيمة الافتراضية هي 0، وهذا يعني عدم وجود مسافة بادئة.

```csharp
public int Count { get; set; }
```

## أمثلة

يوضح كيفية تكوين المسافة البادئة للقائمة عند حفظ مستند إلى نص عادي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أنشئ قائمة بثلاثة مستويات من المسافة البادئة.
builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent(); 
builder.Write("Item 3");

// قم بإنشاء كائن "TxtSaveOptions"، والذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية حفظ المستند إلى نص عادي.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// قم بتعيين خاصية "الحرف" لتعيين حرف لاستخدامه
// للحشوة التي تحاكي المسافة البادئة للقائمة في النص العادي.
txtSaveOptions.ListIndentation.Character = ' ';

// قم بتعيين خاصية "العدد" لتحديد عدد المرات
// لوضع حرف الحشو لكل مستوى من مستويات المسافة البادئة في القائمة.
txtSaveOptions.ListIndentation.Count = 3;

doc.Save(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt");

Assert.AreEqual("1. Item 1\r\n" +
                "   a. Item 2\r\n" +
                "      i. Item 3\r\n", docText);
```

### أنظر أيضا

* class [TxtListIndentation](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
