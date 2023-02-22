---
title: HtmlSaveOptions.FontResourcesSubsettingSizeThreshold
second_title: Aspose.Words لمراجع .NET API
description: HtmlSaveOptions ملكية. يتحكم في تحديد موارد الخط التي تحتاج إلى تعيين عند الحفظ بتنسيق HTML أو MHTML أو EPUB . الإعداد الافتراضي هو0 .
type: docs
weight: 300
url: /ar/net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

يتحكم في تحديد موارد الخط التي تحتاج إلى تعيين عند الحفظ بتنسيق HTML أو MHTML أو EPUB . الإعداد الافتراضي هو`0` .

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

### ملاحظات

[`ExportFontResources`](../exportfontresources/) يسمح بتصدير الخطوط كملفات فرعية أو كجزء من حزمة output . إذا كان المستند يستخدم العديد من الخطوط ، خاصة مع وجود عدد كبير من الحروف الرسومية ، فيمكن أن ينمو حجم الإخراج بشكل ملحوظ. يقلل تقليل حجم الخط من حجم مصدر الخط الذي تم تصديره عن طريق تصفية الحروف الرسومية التي لا يتم استخدامها في المستند الحالي.

يعمل تقسيم الخط على النحو التالي:

* بشكل افتراضي ، تكون كل الخطوط المصدرة جزئية.
* ضبط`FontResourcesSubsettingSizeThreshold`إلى قيمة موجبة يوجه Aspose.Words مجموعة فرعية من الخطوط التي يكون حجم الملف فيها أكبر من القيمة المحددة.
* تعيين الخاصية إلىMaxValue يمنع تعيين الخط.

**مهم!** عند تصدير موارد الخطوط ، يجب مراعاة مشكلات ترخيص الخطوط. يجب على المؤلفين الذين يرغبون في استخدام خطوط معينة عبر آلية خط downloadable التحقق بعناية دائمًا من أن الاستخدام المقصود يقع ضمن نطاق ترخيص الخط. لا تسمح العديد من الخطوط التجارية حاليًا بتنزيل الويب لخطوطها بأي شكل من الأشكال. تشير اتفاقيات الترخيص التي تغطي بعض الخطوط تحديدًا إلى أن الاستخدام عبر **@ font-face** القواعد في أوراق أنماط CSS غير مسموح بها. يمكن أن ينتهك تقسيم الخط أيضًا شروط الترخيص.

### أمثلة

يوضح كيفية العمل مع تقليل حجم الخط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Times New Roman";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("Hello world!");

// عندما نحفظ المستند إلى HTML ، يمكننا تمرير إعداد فرعي للخط لكائن SaveOptions.
// لنفترض أننا قمنا بتعيين علامة "ExportFontResources" على "true" وقمنا أيضًا بتسمية مجلد في خاصية "FontsFolder".
// في هذه الحالة ، ستنشئ عملية الحفظ هذا المجلد وتضع ملف .ttf بداخله
// هذا المجلد لكل خط تستخدمه وثيقتنا.
// سيحتوي كل ملف .ttf على مجموعة الحروف الرسومية الكاملة لهذا الخط ،
// مما قد ينتج عنه ملف كبير جدًا مرفق بالمستند.
// عندما نطبق التقسيم إلى خط ما ، فإن بياناته الأولية التي تم تصديرها ستحتوي فقط على الحروف الرسومية الموجودة في المستند
// باستخدام بدلاً من مجموعة الحروف الرسومية بأكملها. إذا كان النص في وثيقتنا يستخدم جزءًا صغيرًا من الخط
// glyph set ، ثم يؤدي التعيين الجزئي إلى تقليل حجم مستندات الإخراج بشكل كبير.
// يمكننا استخدام خاصية "FontResourcesSubsettingSizeThreshold" لتحديد حجم ملف .ttf بالبايت.
 // إذا كان الخط الذي تم تصديره ينشئ ملفًا بحجم أكبر من ذلك ، فسيتم تطبيق عملية الحفظ على هذا الخط.
// تعيين عتبة 0 يطبق التقسيم على جميع الخطوط ،
// وتعيينه على "int.MaxValue" يعطل التعيين بشكل فعال.
string fontsFolder = ArtifactsDir + "HtmlSaveOptions.FontSubsetting.Fonts";

HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportFontResources = true,
    FontsFolder = fontsFolder,
    FontResourcesSubsettingSizeThreshold = fontResourcesSubsettingSizeThreshold
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FontSubsetting.html", options);

string[] fontFileNames = Directory.GetFiles(fontsFolder).Where(s => s.EndsWith(".ttf")).ToArray();

Assert.AreEqual(3, fontFileNames.Length);

foreach (string filename in fontFileNames)
{
    // بشكل افتراضي ، سيكون حجم ملفات .ttf لكل من خطوطنا الثلاثة أكثر من 700 ميجابايت.
    // سيؤدي التقليل إلى تقليلها جميعًا إلى أقل من 30 ميغا بايت.
    FileInfo fontFileInfo = new FileInfo(filename);

    Assert.True(fontFileInfo.Length > 700000 || fontFileInfo.Length < 30000);
    Assert.True(Math.Max(fontResourcesSubsettingSizeThreshold, 30000) > new FileInfo(filename).Length);
}
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions/)
* المجسم [Aspose.Words](../../../)


