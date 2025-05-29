---
title: DocumentBuilder.ListFormat
linktitle: ListFormat
articleTitle: ListFormat
second_title: Aspose.Words لـ .NET
description: استكشف خاصية ListFormat في DocumentBuilder للوصول إلى إعدادات تنسيق القائمة الحالية وتخصيصها لتحسين تصميم المستند.
type: docs
weight: 150
url: /ar/net/aspose.words/documentbuilder/listformat/
---
## DocumentBuilder.ListFormat property

يعيد كائنًا يمثل خصائص تنسيق القائمة الحالية.

```csharp
public ListFormat ListFormat { get; }
```

## أمثلة

يوضح كيفية إنشاء قوائم مرقمة ومنقطة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Aspose.Words main advantages are:");

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات باستخدام رموز البادئة والمسافات البادئة.
 //يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة.
 // يمكننا أن نبدأ وننهي القائمة باستخدام خاصية "ListFormat" الموجودة في منشئ المستندات.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// فيما يلي نوعان من القوائم التي يمكننا إنشاؤها باستخدام منشئ المستندات.
// 1 - قائمة نقطية:
// ستطبق هذه القائمة مسافة بادئة ورمز نقطي ("•") قبل كل فقرة.
builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Great performance");
builder.Writeln("High reliability");
builder.Writeln("Quality code and working");
builder.Writeln("Wide variety of features");
builder.Writeln("Easy to understand API");

//إنهاء القائمة النقطية.
builder.ListFormat.RemoveNumbers();

builder.InsertBreak(BreakType.ParagraphBreak);
builder.Writeln("Aspose.Words allows:");

// 2 - قائمة مرقمة:
// تقوم القوائم المرقمة بإنشاء ترتيب منطقي لفقراتها عن طريق ترقيم كل عنصر.
builder.ListFormat.ApplyNumberDefault();

// هذه الفقرة هي العنصر الأول. العنصر الأول في القائمة المرقمة سيحمل الرمز "1".
builder.Writeln("Opening documents from different formats:");

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

//استدعاء طريقة "ListIndent" لزيادة مستوى القائمة الحالية،
// والتي ستبدأ قائمة مستقلة جديدة، بمسافة بادئة أعمق، في العنصر الحالي لمستوى القائمة الأول.
builder.ListFormat.ListIndent();

Assert.AreEqual(1, builder.ListFormat.ListLevelNumber);

// هذه هي العناصر الثلاثة الأولى في القائمة من المستوى الثاني للقائمة، والتي ستحافظ على عدد
// بغض النظر عن عدد المستويات في القائمة الأولى. وفقًا لتنسيق القائمة الحالي،
// سيكون لديهم رموز "أ"، "ب"، و"ج".
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");

// قم باستدعاء طريقة "ListOutdent" للعودة إلى مستوى القائمة السابق.
builder.ListFormat.ListOutdent();

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// هاتان الفقرتان ستواصلان حساب مستوى القائمة الأول.
// ستحمل هذه العناصر رموز "2."، و"3."
builder.Writeln("Processing documents");
builder.Writeln("Saving documents in different formats:");

// إذا قمنا بزيادة مستوى القائمة إلى المستوى الذي أضفنا إليه العناصر سابقًا،
 // ستكون القائمة المتداخلة منفصلة عن القائمة السابقة، وسيبدأ ترقيمها من البداية.
// ستحتوي عناصر القائمة هذه على رموز "أ"، "ب"، "ج"، "د"، و"هـ".
builder.ListFormat.ListIndent();
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");
builder.Writeln("MHTML");
builder.Writeln("Plain text");

// قم برفع مستوى القائمة مرة أخرى.
builder.ListFormat.ListOutdent();
builder.Writeln("Doing many other things!");

//إنهاء القائمة المرقمة.
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.ApplyDefaultBulletsAndNumbers.docx");
```

### أنظر أيضا

* class [ListFormat](../../../aspose.words.lists/listformat/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
