---
title: HtmlSaveOptions.EpubNavigationMapLevel
second_title: Aspose.Words لمراجع .NET API
description: HtmlSaveOptions ملكية. يحدد المستوى الأقصى للعناوين التي يتم ملؤها في خريطة التنقل عند التصدير إلى تنسيق IDPF EPUB . القيمة الافتراضية هي3 .
type: docs
weight: 110
url: /ar/net/aspose.words.saving/htmlsaveoptions/epubnavigationmaplevel/
---
## HtmlSaveOptions.EpubNavigationMapLevel property

يحدد المستوى الأقصى للعناوين التي يتم ملؤها في خريطة التنقل عند التصدير إلى تنسيق IDPF EPUB . القيمة الافتراضية هي`3` .

```csharp
public int EpubNavigationMapLevel { get; set; }
```

### ملاحظات

تتيح خريطة التنقل بتنسيق IDPF EPUB لوكلاء المستخدم توفير طريقة سهلة للتنقل من خلال بنية المستند. عادةً ما تتوافق نقاط التنقل مع العناوين الموجودة في المستند. لتعبئة العناوين حتى المستوى **ن** إسناد هذه القيمة إلى`EpubNavigationMapLevel`.

بشكل افتراضي ، يتم ملء ثلاثة مستويات من العناوين: فقرات الأنماط **عنوان 1** و **العنوان 2** و **العنوان 3**. يمكنك تعيين هذه الخاصية إلى قيمة من 1 إلى 9 لطلب المستوى الأقصى المقابل. سيؤدي تعيينه إلى الصفر إلى تقليل خريطة التنقل لتقتصر على جذر المستند أو جذور أجزاء المستند فقط.

### أمثلة

يوضح كيفية تصفية العناوين التي تظهر في لوحة التنقل لمستند Epub المحفوظ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// كل فقرة نقوم بتنسيقها باستخدام نمط "العنوان" يمكن أن تكون بمثابة عنوان.
// قد يكون لكل عنوان أيضًا مستوى عنوان محدد بواسطة رقم نمط العنوان الخاص به.
// العناوين أدناه من المستويات 1-3.
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #1");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #2");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #3");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #4");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #5");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #6");

// يقوم قراء Epub عادةً بإنشاء جدول محتويات لمستنداتهم.
// كل فقرة بنمط "عنوان" في المستند ستنشئ إدخالاً في جدول المحتويات هذا.
 // يمكننا استخدام خاصية "EpubNavigationMapLevel" لتعيين الحد الأقصى لمستوى العنوان.
// لن يضيف قارئ Epub عناوين بمستوى أعلى من المستوى الذي نحدده في جدول المحتويات.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Epub);
options.EpubNavigationMapLevel = 2;

// تحتوي وثيقتنا على ستة عناوين ، اثنان منها فوق المستوى 2.
// سيتضمن جدول محتويات هذا المستند أربعة مداخل.
doc.Save(ArtifactsDir + "HtmlSaveOptions.EpubHeadings.epub", options);
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions/)
* المجسم [Aspose.Words](../../../)


