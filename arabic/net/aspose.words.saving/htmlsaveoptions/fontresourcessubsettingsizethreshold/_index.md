---
title: HtmlSaveOptions.FontResourcesSubsettingSizeThreshold
second_title: Aspose.Words لمراجع .NET API
description: HtmlSaveOptions ملكية. يتحكم في موارد الخطوط التي تحتاج إلى تعيين فرعي عند الحفظ في HTML أو MHTML أو EPUB. الإعداد الافتراضي هو0 .
type: docs
weight: 290
url: /ar/net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

يتحكم في موارد الخطوط التي تحتاج إلى تعيين فرعي عند الحفظ في HTML أو MHTML أو EPUB. الإعداد الافتراضي هو`0` .

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

### ملاحظات

[`ExportFontResources`](../exportfontresources/) يسمح بتصدير الخطوط كملفات فرعية أو كأجزاء من حزمة الإخراج . إذا كانت الوثيقة تستخدم العديد من الخطوط، خاصة مع عدد كبير من الحروف الرسومية، فيمكن أن ينمو حجم الإخراج بشكل ملحوظ. يعمل الإعداد الفرعي للخط على تقليل حجم مصدر الخط المصدر عن طريق تصفية الصور الرمزية التي لا يستخدمها المستند الحالي .

يعمل الإعداد الفرعي للخط على النحو التالي:

* بشكل افتراضي، يتم تعيين كافة الخطوط المصدرة فرعيًا.
* جلسة`FontResourcesSubsettingSizeThreshold`إلى قيمة موجبة يرشد Aspose.Words إلى تعيين الخطوط التي يكون حجم الملف فيها أكبر من القيمة المحددة.
* ضبط العقار علىMaxValue يمنع ضبط الخط الفرعي.

**مهم!** عند تصدير موارد الخطوط، يجب مراعاة مشكلات ترخيص الخطوط. يجب على المؤلفين الذين يرغبون في استخدام خطوط معينة عبر آلية الخط القابلة للتنزيل أن يتحققوا دائمًا بعناية من أن الاستخدام المقصود يقع ضمن نطاق ترخيص الخط. لا تسمح العديد من الخطوط التجارية في الوقت الحالي بتنزيل خطوطها من الويب بأي شكل من الأشكال. تشير اتفاقيات الترخيص التي تغطي بعض الخطوط على وجه التحديد إلى أن الاستخدام عبر **@الخط الوجه** Rules غير مسموح به في أوراق أنماط CSS. يمكن أن يؤدي تعيين الخط الفرعي أيضًا إلى انتهاك شروط الترخيص.

### أمثلة

يوضح كيفية العمل مع ضبط الخط الفرعي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Times New Roman";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("Hello world!");

// عندما نحفظ المستند إلى HTML، يمكننا تمرير إعداد فرعي للخط لكائن SaveOptions.
// لنفترض أننا قمنا بتعيين علامة "ExportFontResources" على "صحيح" وقمنا أيضًا بتسمية مجلد في خاصية "FontsFolder".
// في هذه الحالة، ستقوم عملية الحفظ بإنشاء هذا المجلد ووضع ملف .ttf بداخله
// هذا المجلد لكل خط يستخدمه وثيقتنا.
// سيحتوي كل ملف .ttf على مجموعة الحروف الرسومية الكاملة لهذا الخط،
// مما قد يؤدي إلى وجود ملف كبير جدًا مصاحب للمستند.
// عندما نطبق الإعداد الفرعي على خط ما، فإن بياناته الأولية المصدرة ستحتوي فقط على الحروف الرسومية الموجودة في المستند
// الاستخدام بدلاً من مجموعة الحروف الرسومية بأكملها. إذا كان النص الموجود في وثيقتنا يستخدم جزءًا صغيرًا فقط من الخط
// مجموعة الحروف الرسومية، فإن الإعداد الفرعي سيقلل بشكل كبير من حجم مستندات الإخراج لدينا.
// يمكننا استخدام خاصية "FontResourcesSubsettingSizeThreshold" لتحديد حجم ملف .ttf بالبايت.
 // إذا قام الخط الذي تم تصديره بإنشاء ملف بحجم أكبر من ذلك، فستطبق عملية الحفظ الإعداد الفرعي على هذا الخط.
// تعيين عتبة 0 يطبق الإعداد الفرعي على كافة الخطوط،
// وتعيينه على "int.MaxValue" يؤدي إلى تعطيل الإعداد الفرعي بشكل فعال.
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
    // بشكل افتراضي، سيكون حجم ملفات .ttf لكل من الخطوط الثلاثة لدينا أكبر من 700 ميجابايت.
    // سيؤدي الإعداد الفرعي إلى تقليل حجمها جميعًا إلى أقل من 30 ميجابايت.
    FileInfo fontFileInfo = new FileInfo(filename);

    Assert.True(fontFileInfo.Length > 700000 || fontFileInfo.Length < 30000);
    Assert.True(Math.Max(fontResourcesSubsettingSizeThreshold, 30000) > new FileInfo(filename).Length);
}
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions/)
* المجسم [Aspose.Words](../../../)


