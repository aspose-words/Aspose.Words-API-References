---
title: PageSetup.MultiplePages
second_title: Aspose.Words لمراجع .NET API
description: PageSetup ملكية. لمستندات متعددة الصفحات  الحصول على أو تعيين كيفية طباعة المستند أو تقديمه بحيث يمكن ربطه ككتيب.
type: docs
weight: 260
url: /ar/net/aspose.words/pagesetup/multiplepages/
---
## PageSetup.MultiplePages property

لمستندات متعددة الصفحات ، الحصول على أو تعيين كيفية طباعة المستند أو تقديمه بحيث يمكن ربطه ككتيب.

```csharp
public MultiplePagesType MultiplePages { get; set; }
```

### أمثلة

يوضح كيفية تكوين مستند يمكن طباعته كطي كتاب.

```csharp
Document doc = new Document();

// أدخل نصًا يمتد عبر 16 صفحة.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// تكوين خاصية "إعداد الصفحة" للقسم الأول لطباعة المستند في شكل طية كتاب.
// عندما نطبع هذا المستند على كلا الجانبين ، يمكننا أن نأخذ الصفحات لتكديسها
// وقم بطيها جميعًا في المنتصف مرة واحدة. ستصطف محتويات المستند في طية كتاب.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// يمكننا فقط تحديد عدد الأوراق بمضاعفات 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

يوضح كيفية تعيين هوامش هامش التوثيق.

```csharp
Document doc = new Document();

// أدخل نصًا يمتد على عدة صفحات.
DocumentBuilder builder = new DocumentBuilder(doc);
for (int i = 0; i < 6; i++)
{
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                  "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder.InsertBreak(BreakType.PageBreak);
}

// يضيف الحضيض مسافات بيضاء إلى هامش الصفحة الأيمن أو الأيسر ،
// مما يعوض عن طي الوسط للصفحات في كتاب يتعدى على تخطيط الصفحة.
PageSetup pageSetup = doc.Sections[0].PageSetup;

 // حدد مقدار المساحة المتوفرة لصفحاتنا للنص داخل الهوامش ثم أضف مقدارًا لتضمين الهامش.
Assert.AreEqual(470.30d, pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, 0.01d);

pageSetup.Gutter = 100.0d;

// اضبط خاصية "RtlGutter" على "true" لوضع هامش التوثيق في موضع أكثر ملاءمة للنص من اليمين إلى اليسار.
pageSetup.RtlGutter = true;

// اضبط خاصية "MultiplePages" على "MultiplePagesType.MirrorMargins" على البديل
// موضع جانب الصفحة الأيسر / الأيمن للهوامش لكل صفحة.
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### أنظر أيضا

* enum [MultiplePagesType](../../../aspose.words.settings/multiplepagestype/)
* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../pagesetup/)
* المجسم [Aspose.Words](../../../)


