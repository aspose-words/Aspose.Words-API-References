---
title: HtmlSaveOptions.FontResourcesSubsettingSizeThreshold
linktitle: FontResourcesSubsettingSizeThreshold
articleTitle: FontResourcesSubsettingSizeThreshold
second_title: Aspose.Words لـ .NET
description: حسّن ملفات HTML أو MHTML أو EPUB باستخدام خاصية FontResourcesSubsettingSizeThreshold، مما يضمن إدارة فعّالة لموارد الخطوط. القيمة الافتراضية: 0.
type: docs
weight: 290
url: /ar/net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

يتحكم في موارد الخط التي تحتاج إلى تعيين فرعي عند الحفظ في HTML أو MHTML أو EPUB. الافتراضي هو`0` .

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

## ملاحظات

[`ExportFontResources`](../exportfontresources/) يسمح بتصدير الخطوط كملفات فرعية أو كجزء من حزمة output . إذا كان المستند يستخدم العديد من الخطوط، خاصةً مع عدد كبير من الحروف، فقد يزداد حجم المخرجات بشكل ملحوظ. يُقلل تقسيم الخطوط حجم مورد الخط المُصدَّر عن طريق تصفية الحروف التي لا يستخدمها المستند الحالي.

تعمل عملية تقسيم الخطوط على النحو التالي:

* بشكل افتراضي، يتم تقسيم كافة الخطوط المصدرة إلى مجموعات فرعية.
* جلسة`FontResourcesSubsettingSizeThreshold` إلى قيمة موجبة يطلب من Aspose.Words تحديد مجموعة فرعية من الخطوط التي يكون حجم ملفها أكبر من القيمة المحددة.
* تعيين الخاصية إلىMaxValue يمنع تقسيم الخطوط.

**مهم!**عند تصدير موارد الخطوط، يجب مراعاة مسائل ترخيص الخطوط. يجب على المؤلفين الراغبين في استخدام خطوط محددة عبر آلية الخطوط القابلة للتنزيل التأكد بعناية من أن استخدامها المقصود يقع ضمن نطاق ترخيص الخطوط. لا تسمح العديد من الخطوط التجارية حاليًا بتنزيل خطوطها من الإنترنت بأي شكل من الأشكال. تنص اتفاقيات الترخيص التي تغطي بعض الخطوط تحديدًا على أن الاستخدام عبر**@الخط-الوجه** لا يُسمح باستخدام rules في أوراق أنماط CSS. قد يُخالف تقسيم الخطوط شروط الترخيص.

## أمثلة

يوضح كيفية العمل مع تقسيم الخطوط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Times New Roman";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("Hello world!");

// عندما نحفظ المستند بصيغة HTML، يمكننا تمرير كائن SaveOptions لتكوين مجموعة فرعية من الخطوط.
// لنفترض أننا قمنا بتعيين علم "ExportFontResources" إلى "true" وقمنا أيضًا بتسمية مجلد في خاصية "FontsFolder".
// في هذه الحالة، ستقوم عملية الحفظ بإنشاء هذا المجلد ووضع ملف .ttf بداخله
//هذا المجلد لكل خط يستخدمه مستندنا.
// سيحتوي كل ملف .ttf على مجموعة الحروف الكاملة لهذا الخط،
// مما قد يؤدي إلى ظهور ملف كبير جدًا مرفق بالمستند.
// عندما نطبق التجزئة على خط، فإن بياناته الخام المُصدرة ستحتوي فقط على الحروف الرسومية التي يحتوي عليها المستند
// باستخدام مجموعة الحروف الرسومية كاملةً بدلاً من استخدامها. إذا كان النص في مستندنا يستخدم جزءًا صغيرًا فقط من حجم الخط،
// مجموعة الحروف الرسومية، ثم سيؤدي تقسيمها إلى مجموعات فرعية إلى تقليل حجم مستندات الإخراج بشكل كبير.
// يمكننا استخدام الخاصية "FontResourcesSubsettingSizeThreshold" لتحديد حجم ملف .ttf، بالبايت.
 // إذا قام الخط المُصدَّر بإنشاء ملف بحجم أكبر من ذلك، فستقوم عملية الحفظ بتطبيق التقسيم الفرعي على هذا الخط.
// يؤدي تعيين حد أدنى بقيمة 0 إلى تطبيق التعيين الفرعي على جميع الخطوط،
// وتعيينه إلى "int.MaxValue" يعطل بشكل فعال عملية التقسيم الفرعي.
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
    // سيؤدي تقسيمها إلى مجموعات فرعية إلى تقليل حجمها جميعًا إلى أقل من 30 ميجابايت.
    FileInfo fontFileInfo = new FileInfo(filename);

    Assert.True(fontFileInfo.Length > 700000 || fontFileInfo.Length < 30000);
    Assert.True(Math.Max(fontResourcesSubsettingSizeThreshold, 30000) > new FileInfo(filename).Length);
}
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
