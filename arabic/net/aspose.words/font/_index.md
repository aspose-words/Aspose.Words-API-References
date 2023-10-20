---
title: Font Class
linktitle: Font
articleTitle: Font
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Font فصل. يحتوي على سمات الخط اسم الخط وحجم الخط واللون وما إلى ذلك لكائن ما في C#.
type: docs
weight: 2830
url: /ar/net/aspose.words/font/
---
## Font class

يحتوي على سمات الخط (اسم الخط وحجم الخط واللون وما إلى ذلك) لكائن ما.

لمعرفة المزيد، قم بزيارة[العمل مع الخطوط](https://docs.aspose.com/words/net/working-with-fonts/) مقالة توثيقية.

```csharp
public class Font
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [AllCaps](../../aspose.words/font/allcaps/) { get; set; } | صحيح إذا كان الخط منسقًا بأحرف كبيرة. |
| [AutoColor](../../aspose.words/font/autocolor/) { get; } | إرجاع اللون المحسوب الحالي للنص (أسود أو أبيض) لاستخدامه في "اللون التلقائي". إذا لم يكن اللون "تلقائيًا"، فسيتم إرجاعه[`Color`](./color/) . |
| [Bidi](../../aspose.words/font/bidi/) { get; set; } | يحدد ما إذا كانت محتويات هذا التشغيل يجب أن تكون ذات خصائص من اليمين إلى اليسار. |
| [Bold](../../aspose.words/font/bold/) { get; set; } | صحيح إذا كان الخط منسقًا بالخط الغامق. |
| [BoldBi](../../aspose.words/font/boldbi/) { get; set; } | صحيح إذا كان النص من اليمين إلى اليسار منسقاً بالخط الغامق. |
| [Border](../../aspose.words/font/border/) { get; } | إرجاع أ[`Border`](../border/) الكائن الذي يحدد الحدود للخط. |
| [Color](../../aspose.words/font/color/) { get; set; } | الحصول على أو تعيين لون الخط. |
| [ComplexScript](../../aspose.words/font/complexscript/) { get; set; } | يحدد ما إذا كان سيتم التعامل مع محتويات هذا التشغيل كنص نصي معقد بغض النظر عن قيم أحرف Unicode الخاصة بها عند تحديد التنسيق لهذا التشغيل. |
| [DoubleStrikeThrough](../../aspose.words/font/doublestrikethrough/) { get; set; } | صحيح إذا تم تنسيق الخط كنص يتوسطه خط مزدوج. |
| [Emboss](../../aspose.words/font/emboss/) { get; set; } | صحيح إذا كان الخط منسقًا بشكل منقوش. |
| [EmphasisMark](../../aspose.words/font/emphasismark/) { get; set; } | الحصول على أو تعيين علامة التركيز المطبقة على هذا التنسيق. |
| [Engrave](../../aspose.words/font/engrave/) { get; set; } | صحيح إذا تم تنسيق الخط على أنه منقوش. |
| [Fill](../../aspose.words/font/fill/) { get; } | يحصل على تنسيق التعبئة لـ`Font` . |
| [Hidden](../../aspose.words/font/hidden/) { get; set; } | صحيح إذا تم تنسيق الخط كنص مخفي. |
| [HighlightColor](../../aspose.words/font/highlightcolor/) { get; set; } | الحصول على أو تعيين لون التمييز (علامة التحديد). |
| [Italic](../../aspose.words/font/italic/) { get; set; } | صحيح إذا كان الخط منسقًا بالخط المائل. |
| [ItalicBi](../../aspose.words/font/italicbi/) { get; set; } | صحيح إذا كان النص من اليمين إلى اليسار منسقاً بالخط المائل. |
| [Kerning](../../aspose.words/font/kerning/) { get; set; } | الحصول على أو تعيين حجم الخط الذي يبدأ عنده تقنين الأحرف. |
| [LineSpacing](../../aspose.words/font/linespacing/) { get; } | إرجاع تباعد الأسطر لهذا الخط (بالنقاط). |
| [LocaleId](../../aspose.words/font/localeid/) { get; set; } | الحصول على أو تعيين المعرف المحلي (اللغة) للأحرف المنسقة. |
| [LocaleIdBi](../../aspose.words/font/localeidbi/) { get; set; } | الحصول على أو تعيين المعرف المحلي (اللغة) للأحرف المنسقة من اليمين إلى اليسار. |
| [LocaleIdFarEast](../../aspose.words/font/localeidfareast/) { get; set; } | الحصول على أو تعيين المعرف المحلي (اللغة) للأحرف الآسيوية المنسقة. |
| [Name](../../aspose.words/font/name/) { get; set; } | الحصول على اسم الخط أو تعيينه. |
| [NameAscii](../../aspose.words/font/nameascii/) { get; set; } | إرجاع أو تعيين الخط المستخدم للنص اللاتيني (الأحرف ذات رموز الأحرف من 0 (صفر) إلى 127). |
| [NameBi](../../aspose.words/font/namebi/) { get; set; } | إرجاع أو تعيين اسم الخط في مستند لغة من اليمين إلى اليسار. |
| [NameFarEast](../../aspose.words/font/namefareast/) { get; set; } | إرجاع أو تعيين اسم خط شرق آسيوي. |
| [NameOther](../../aspose.words/font/nameother/) { get; set; } | إرجاع أو تعيين الخط المستخدم للأحرف ذات رموز الأحرف من 128 إلى 255. |
| [NoProofing](../../aspose.words/font/noproofing/) { get; set; } | صحيح عندما لا يتم التدقيق الإملائي على الأحرف المنسقة. |
| [Outline](../../aspose.words/font/outline/) { get; set; } | صحيح إذا تم تنسيق الخط كمخطط تفصيلي. |
| [Position](../../aspose.words/font/position/) { get; set; } | الحصول على أو تعيين موضع النص (بالنقاط) بالنسبة إلى السطر الأساسي. الرقم الموجب يرفع النص، والرقم السالب يخفضه. |
| [Scaling](../../aspose.words/font/scaling/) { get; set; } | الحصول على أو تعيين مقياس عرض الأحرف بالنسبة المئوية. |
| [Shading](../../aspose.words/font/shading/) { get; } | إرجاع أ[`Shading`](../shading/) الكائن الذي يشير إلى تنسيق التظليل للخط. |
| [Shadow](../../aspose.words/font/shadow/) { get; set; } | صحيح إذا تم تنسيق الخط على أنه مظلل. |
| [Size](../../aspose.words/font/size/) { get; set; } | الحصول على حجم الخط أو تعيينه بالنقاط. |
| [SizeBi](../../aspose.words/font/sizebi/) { get; set; } | الحصول على حجم الخط أو تعيينه بالنقاط المستخدمة في مستند من اليمين إلى اليسار. |
| [SmallCaps](../../aspose.words/font/smallcaps/) { get; set; } | صحيح إذا تم تنسيق الخط بأحرف كبيرة صغيرة. |
| [SnapToGrid](../../aspose.words/font/snaptogrid/) { get; set; } | يحدد ما إذا كان الخط الحالي يجب أن يستخدم أحرف شبكة المستند لكل إعدادات السطر عند التخطيط. |
| [Spacing](../../aspose.words/font/spacing/) { get; set; } | إرجاع أو ضبط التباعد (بالنقاط) بين الأحرف . |
| [StrikeThrough](../../aspose.words/font/strikethrough/) { get; set; } | صحيح إذا تم تنسيق الخط كنص يتوسطه خط. |
| [Style](../../aspose.words/font/style/) { get; set; } | الحصول على أو تعيين نمط الأحرف المطبق على هذا التنسيق. |
| [StyleIdentifier](../../aspose.words/font/styleidentifier/) { get; set; } | الحصول على أو تعيين معرف النمط المحلي المستقل لنمط الأحرف المطبق على هذا التنسيق. |
| [StyleName](../../aspose.words/font/stylename/) { get; set; } | الحصول على أو تعيين اسم نمط الأحرف المطبق على هذا التنسيق. |
| [Subscript](../../aspose.words/font/subscript/) { get; set; } | صحيح إذا تم تنسيق الخط كخط منخفض. |
| [Superscript](../../aspose.words/font/superscript/) { get; set; } | صحيح إذا تم تنسيق الخط كخط مرتفع. |
| [TextEffect](../../aspose.words/font/texteffect/) { get; set; } | الحصول على تأثير الخط المتحرك أو تعيينه. |
| [ThemeColor](../../aspose.words/font/themecolor/) { get; set; } | الحصول على أو تعيين لون السمة في نظام الألوان المطبق المرتبط بهذا`Font` الكائن. |
| [ThemeFont](../../aspose.words/font/themefont/) { get; set; } | الحصول على أو تعيين خط السمة في نظام الخطوط المطبق المرتبط بهذا`Font` الكائن. |
| [ThemeFontAscii](../../aspose.words/font/themefontascii/) { get; set; } | الحصول على أو تعيين خط السمة المستخدم للنص اللاتيني (الأحرف ذات رموز الأحرف من 0 (صفر) إلى 127) في نظام الخطوط المطبق المرتبط بهذا`Font` الكائن. |
| [ThemeFontBi](../../aspose.words/font/themefontbi/) { get; set; } | الحصول على أو تعيين خط السمة في نظام الخطوط المطبق المرتبط بهذا`Font` object في مستند لغة من اليمين إلى اليسار. |
| [ThemeFontFarEast](../../aspose.words/font/themefontfareast/) { get; set; } | الحصول على أو تعيين خط سمة شرق آسيا في نظام الخطوط المطبق المرتبط بهذا`Font` الكائن. |
| [ThemeFontOther](../../aspose.words/font/themefontother/) { get; set; } | الحصول على أو تعيين خط السمة المستخدم للأحرف ذات رموز الأحرف من 128 إلى 255 في نظام الخطوط المطبق المرتبط بهذا`Font` الكائن. |
| [TintAndShade](../../aspose.words/font/tintandshade/) { get; set; } | الحصول على أو تعيين قيمة مزدوجة تعمل على تفتيح اللون أو تغميقه. |
| [Underline](../../aspose.words/font/underline/) { get; set; } | الحصول على أو تعيين نوع التسطير المطبق على الخط. |
| [UnderlineColor](../../aspose.words/font/underlinecolor/) { get; set; } | الحصول على أو تعيين لون التسطير المطبق على الخط. |

## طُرق

| اسم | وصف |
| --- | --- |
| [ClearFormatting](../../aspose.words/font/clearformatting/)() | إعادة التعيين إلى تنسيق الخط الافتراضي. |
| [HasDmlEffect](../../aspose.words/font/hasdmleffect/)(*[TextDmlEffect](../textdmleffect/)*) | للتحقق من تطبيق تأثير نص معين لـ DrawML. |

## ملاحظات

لا تقم بإنشاء مثيلات لـ`Font`الصف مباشرة. أنت فقط تستخدم `Font` للوصول إلى خصائص الخط للكائنات المختلفة مثل[`Run`](../run/)[`Paragraph`](../paragraph/) ,[`Style`](../style/) ,[`DocumentBuilder`](../documentbuilder/).

## أمثلة

يوضح كيفية تنسيق مجموعة من النص باستخدام خاصية الخط الخاصة به.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

يوضح كيفية إدراج سلسلة محاطة بحد في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

يوضح كيفية إنشاء نمط فقرة واستخدامه بتنسيق القائمة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إنشاء نمط فقرة مخصص.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// أنشئ قائمة وتأكد من أن الفقرات التي تستخدم هذا النمط ستستخدم هذه القائمة.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// قم بتطبيق نمط الفقرة على الفقرة الحالية لمنشئ المستند، ثم قم بإضافة بعض النص.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// قم بتغيير نمط منشئ المستندات إلى نمط لا يحتوي على تنسيق قائمة واكتب فقرة أخرى.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
