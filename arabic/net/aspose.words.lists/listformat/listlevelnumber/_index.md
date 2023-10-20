---
title: ListFormat.ListLevelNumber
linktitle: ListLevelNumber
articleTitle: ListLevelNumber
second_title: Aspose.Words لـ .NET
description: ListFormat ListLevelNumber ملكية. الحصول على أو تعيين رقم مستوى القائمة 0 إلى 8 للفقرة في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.lists/listformat/listlevelnumber/
---
## ListFormat.ListLevelNumber property

الحصول على أو تعيين رقم مستوى القائمة (0 إلى 8) للفقرة.

```csharp
public int ListLevelNumber { get; set; }
```

## ملاحظات

في مستندات Word، قد تتكون القوائم من 1 أو 9 مستويات، مرقمة من 0 إلى 8.

لا يكون له تأثير إلا عندما[`List`](../list/) تم تعيين الخاصية للإشارة إلى قائمة صالحة.

## أمثلة

يوضح كيفية العمل مع مستويات القائمة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات برموز البادئة والمسافات البادئة.
 // يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة.
 // يمكننا بدء القائمة وإنهائها باستخدام خاصية "ListFormat" الخاصة بمنشئ المستندات.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// فيما يلي نوعان من القوائم التي يمكننا إنشاؤها باستخدام أداة إنشاء المستندات.
// 1 - قائمة مرقمة:
// تنشئ القوائم المرقمة ترتيبًا منطقيًا لفقراتها عن طريق ترقيم كل عنصر.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// من خلال تعيين خاصية "ListLevelNumber"، يمكننا زيادة مستوى القائمة
// لبدء قائمة فرعية قائمة بذاتها في عنصر القائمة الحالي.
// يستخدم قالب قائمة Microsoft Word المسمى "NumberDefault" الأرقام لإنشاء مستويات القائمة لمستوى القائمة الأول.
 // تستخدم مستويات القائمة الأعمق الحروف والأرقام الرومانية الصغيرة.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - قائمة ذات تعداد نقطي:
// ستطبق هذه القائمة مسافة بادئة ورمز نقطي ("•") قبل كل فقرة.
// ستستخدم المستويات الأعمق لهذه القائمة رموزًا مختلفة، مثل "■" و"○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// يمكننا تعطيل تنسيق القائمة لعدم تنسيق أي فقرات لاحقة كقوائم عن طريق إلغاء تعيين علامة "القائمة".
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

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
* مساحة الاسم [Aspose.Words.Lists](../../../aspose.words.lists/)
* المجسم [Aspose.Words](../../../)
