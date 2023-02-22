---
title: TxtSaveOptions.ListIndentation
second_title: Aspose.Words لمراجع .NET API
description: TxtSaveOptions ملكية. الحصول على كائن ListIndentation الذي يحدد عدد الأحرف التي يجب استخدامها والمسافة البادئة لمستويات القائمة.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/txtsaveoptions/listindentation/
---
## TxtSaveOptions.ListIndentation property

الحصول على كائن ListIndentation الذي يحدد عدد الأحرف التي يجب استخدامها والمسافة البادئة لمستويات القائمة.

```csharp
public TxtListIndentation ListIndentation { get; }
```

### أمثلة

يوضح كيفية تكوين مسافة بادئة للقائمة عند حفظ مستند إلى نص عادي.

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

// قم بإنشاء كائن "TxtSaveOptions" ، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية حفظ المستند على نص عادي.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// قم بتعيين خاصية "الحرف" لتعيين حرف لاستخدامه
// للحشو الذي يحاكي المسافة البادئة للقائمة في نص عادي.
txtSaveOptions.ListIndentation.Character = ' ';

// قم بتعيين خاصية "Count" لتحديد عدد المرات
// لوضع حرف المساحة المتروكة لكل مستوى مسافة بادئة للقائمة.
txtSaveOptions.ListIndentation.Count = 3;

doc.Save(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt");

Assert.AreEqual("1. Item 1\r\n" +
                "   a. Item 2\r\n" +
                "      i. Item 3\r\n", docText);
```

### أنظر أيضا

* class [TxtListIndentation](../../txtlistindentation/)
* class [TxtSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../txtsaveoptions/)
* المجسم [Aspose.Words](../../../)


