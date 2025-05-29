---
title: TxtSaveOptions.SimplifyListLabels
linktitle: SimplifyListLabels
articleTitle: SimplifyListLabels
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل ميزة SimplifyListLabels في TxtSaveOptions على تعزيز الوضوح من خلال تبسيط تسميات القائمة المعقدة لتحسين تمثيل النص.
type: docs
weight: 70
url: /ar/net/aspose.words.saving/txtsaveoptions/simplifylistlabels/
---
## TxtSaveOptions.SimplifyListLabels property

يحدد ما إذا كان يجب على البرنامج تبسيط تسميات القائمة في حالة عدم تمثيل تنسيق التسمية المعقدة بشكل كافٍ بواسطة نص عادي.

إذا تم ضبطه على`حقيقي` تُكتب تسميات القوائم المرقمة بتنسيق رقمي بسيط ، وتُكتب تسميات القوائم المفصلة كأحرف ASCII بسيطة. القيمة الافتراضية هي`خطأ شنيع`.

```csharp
public bool SimplifyListLabels { get; set; }
```

## أمثلة

يوضح كيفية تغيير مظهر القوائم عند حفظ مستند في نص عادي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء قائمة نقطية تحتوي على خمسة مستويات من المسافة البادئة.
builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent();
builder.Writeln("Item 3");
builder.ListFormat.ListIndent();
builder.Writeln("Item 4");
builder.ListFormat.ListIndent();
builder.Write("Item 5");

// قم بإنشاء كائن "TxtSaveOptions"، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية حفظ المستند إلى نص عادي.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// اضبط خاصية "SimplifyListLabels" على "true" لتحويل بعض القوائم
// تحويل الرموز إلى أحرف ASCII أبسط، مثل '*'، 'o'، '+'، '>'، وما إلى ذلك.
// قم بضبط خاصية "SimplifyListLabels" على "false" للحفاظ على أكبر عدد ممكن من رموز القائمة الأصلية.
txtSaveOptions.SimplifyListLabels = simplifyListLabels;

doc.Save(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt");

string newLine = Environment.NewLine;

if (simplifyListLabels)
    Assert.AreEqual($"* Item 1{newLine}" +
                    $"  > Item 2{newLine}" +
                    $"    + Item 3{newLine}" +
                    $"      - Item 4{newLine}" +
                    $"        o Item 5{newLine}", docText);
else
    Assert.AreEqual($"· Item 1{newLine}" +
                    $"o Item 2{newLine}" +
                    $"§ Item 3{newLine}" +
                    $"· Item 4{newLine}" +
                    $"o Item 5{newLine}", docText);
```

### أنظر أيضا

* class [TxtSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
