---
title: ListFormat.ListOutdent
second_title: Aspose.Words لمراجع .NET API
description: ListFormat طريقة. تقليل مستوى القائمة للفقرة الحالية بمقدار مستوى واحد.
type: docs
weight: 80
url: /ar/net/aspose.words.lists/listformat/listoutdent/
---
## ListFormat.ListOutdent method

تقليل مستوى القائمة للفقرة الحالية بمقدار مستوى واحد.

```csharp
public void ListOutdent()
```

### ملاحظات

تقوم هذه الطريقة بتغيير مستوى القائمة وتطبيق خصائص التنسيق للمستوى الجديد.

في مستندات Word، قد تتكون القوائم من تسعة مستويات كحد أقصى. تحدد قائمة formatting لكل مستوى التعداد النقطي أو الرقم المستخدم، والمسافة البادئة اليسرى، والمسافة بين التعداد النقطي والنص وما إلى ذلك.

### أمثلة

يوضح كيفية إنشاء قوائم ذات تعداد نقطي ومرقمة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Aspose.Words main advantages are:");

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات برموز البادئة والمسافات البادئة.
 // يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة.
 // يمكننا بدء القائمة وإنهائها باستخدام خاصية "ListFormat" الخاصة بمنشئ المستندات.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// يوجد أدناه نوعان من القوائم التي يمكننا إنشاؤها باستخدام أداة إنشاء المستندات.
// 1 - قائمة ذات تعداد نقطي:
// ستطبق هذه القائمة مسافة بادئة ورمز نقطي ("•") قبل كل فقرة.
builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Great performance");
builder.Writeln("High reliability");
builder.Writeln("Quality code and working");
builder.Writeln("Wide variety of features");
builder.Writeln("Easy to understand API");

// إنهاء القائمة ذات التعداد النقطي.
builder.ListFormat.RemoveNumbers();

builder.InsertBreak(BreakType.ParagraphBreak);
builder.Writeln("Aspose.Words allows:");

// 2 - قائمة مرقمة:
// تنشئ القوائم المرقمة ترتيبًا منطقيًا لفقراتها عن طريق ترقيم كل عنصر.
builder.ListFormat.ApplyNumberDefault();

// هذه الفقرة هي العنصر الأول. العنصر الأول في القائمة ذات التعداد الرقمي سيكون له الرقم "1". كرمز عنصر القائمة الخاص به.
builder.Writeln("Opening documents from different formats:");

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// اتصل بطريقة "ListIndent" لزيادة مستوى القائمة الحالية،
// والتي ستبدأ قائمة جديدة قائمة بذاتها، مع مسافة بادئة أعمق، عند العنصر الحالي من مستوى القائمة الأول.
builder.ListFormat.ListIndent();

Assert.AreEqual(1, builder.ListFormat.ListLevelNumber);

// هذه هي عناصر القائمة الثلاثة الأولى من مستوى القائمة الثاني، والتي ستحتفظ بالعدد
// مستقل عن عدد مستوى القائمة الأول. وفقا لشكل القائمة الحالية،
// سيكون لديهم رموز "أ" و"ب" و"ج".
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");

// اتصل بطريقة "ListOutdent" للعودة إلى مستوى القائمة السابق.
builder.ListFormat.ListOutdent();

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// ستستمر هاتان الفقرتان في حساب مستوى القائمة الأول.
// ستحتوي هذه العناصر على الرمزين "2" و"3".
builder.Writeln("Processing documents");
builder.Writeln("Saving documents in different formats:");

// إذا قمنا بزيادة مستوى القائمة إلى المستوى الذي أضفنا إليه عناصر سابقًا،
 // القائمة المتداخلة ستكون منفصلة عن القائمة السابقة، وسيبدأ ترقيمها من البداية.
// ستحتوي عناصر القائمة هذه على رموز "a." و"b." و"c." و"d." و"e".
builder.ListFormat.ListIndent();
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");
builder.Writeln("MHTML");
builder.Writeln("Plain text");

// قم بتجاوز مستوى القائمة مرة أخرى.
builder.ListFormat.ListOutdent();
builder.Writeln("Doing many other things!");

// إنهاء القائمة المرقمة.
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.ApplyDefaultBulletsAndNumbers.docx");
```

### أنظر أيضا

* class [ListFormat](../)
* مساحة الاسم [Aspose.Words.Lists](../../listformat/)
* المجسم [Aspose.Words](../../../)


