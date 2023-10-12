---
title: TxtSaveOptions.SimplifyListLabels
second_title: Aspose.Words لمراجع .NET API
description: TxtSaveOptions ملكية. يحدد ما إذا كان يجب على البرنامج تبسيط تسميات القائمة في حالة عدم تمثيل تنسيق التسمية المعقد بشكل مناسب بنص عادي.
type: docs
weight: 70
url: /ar/net/aspose.words.saving/txtsaveoptions/simplifylistlabels/
---
## TxtSaveOptions.SimplifyListLabels property

يحدد ما إذا كان يجب على البرنامج تبسيط تسميات القائمة في حالة عدم تمثيل تنسيق التسمية المعقد بشكل مناسب بنص عادي.

إذا تم تعيينه على`حقيقي` ، تتم كتابة تسميات القائمة المرقمة بتنسيق رقمي بسيط وتسميات القائمة المفصلة كأحرف ASCII بسيطة. القيمة الافتراضية هي`خطأ شنيع`.

```csharp
public bool SimplifyListLabels { get; set; }
```

### أمثلة

يوضح كيفية تغيير مظهر القوائم عند حفظ مستند إلى نص عادي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء قائمة ذات تعداد نقطي بخمسة مستويات من المسافة البادئة.
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

// قم بإنشاء كائن "TxtSaveOptions"، والذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية حفظ المستند إلى نص عادي.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// اضبط خاصية "SimplifyListLabels" على "صحيح" لتحويل بعض القوائم
// تحويل الرموز إلى أحرف ASCII أبسط، مثل '*'، و'o'، و'+'، و'>'، وما إلى ذلك.
// اضبط الخاصية "SimplifyListLabels" على "خطأ" للاحتفاظ بأكبر عدد ممكن من رموز القائمة الأصلية.
txtSaveOptions.SimplifyListLabels = simplifyListLabels;

doc.Save(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt");

if (simplifyListLabels)
    Assert.AreEqual("* Item 1\r\n" +
                    "  > Item 2\r\n" +
                    "    + Item 3\r\n" +
                    "      - Item 4\r\n" +
                    "        o Item 5\r\n", docText);
else
    Assert.AreEqual("· Item 1\r\n" +
                    "o Item 2\r\n" +
                    "§ Item 3\r\n" +
                    "· Item 4\r\n" +
                    "o Item 5\r\n", docText);
```

### أنظر أيضا

* class [TxtSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../txtsaveoptions/)
* المجسم [Aspose.Words](../../../)


