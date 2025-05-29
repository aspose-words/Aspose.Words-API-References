---
title: Font Class
linktitle: Font
articleTitle: Font
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Font، التي تتميز بسمات الخط الأساسية مثل الاسم والحجم واللون لتحسين تنسيق مستندك وتصميمه.
type: docs
weight: 3240
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
| [AllCaps](../../aspose.words/font/allcaps/) { get; set; } | صحيح إذا تم تنسيق الخط بأحرف كبيرة. |
| [AutoColor](../../aspose.words/font/autocolor/) { get; } | يعيد اللون المحسوب الحالي للنص (أسود أو أبيض) الذي سيتم استخدامه لـ "اللون التلقائي". إذا لم يكن اللون "تلقائيًا"، فيتم إرجاع[`Color`](./color/) . |
| [Bidi](../../aspose.words/font/bidi/) { get; set; } | يحدد ما إذا كان محتوى هذا التشغيل يجب أن يحتوي على خصائص من اليمين إلى اليسار. |
| [Bold](../../aspose.words/font/bold/) { get; set; } | صحيح إذا تم تنسيق الخط على أنه غامق. |
| [BoldBi](../../aspose.words/font/boldbi/) { get; set; } | صحيح إذا تم تنسيق النص من اليمين إلى اليسار بالخط العريض. |
| [Border](../../aspose.words/font/border/) { get; } | يعيد[`Border`](../border/) الكائن الذي يحدد حدود الخط. |
| [Color](../../aspose.words/font/color/) { get; set; } | يحصل على لون الخط أو يعينه. |
| [ComplexScript](../../aspose.words/font/complexscript/) { get; set; } | يحدد ما إذا كان سيتم التعامل مع محتويات هذا التشغيل كنص نصي معقد بغض النظر عن قيم أحرف Unicode الخاصة بها عند تحديد التنسيق لهذا التشغيل. |
| [DoubleStrikeThrough](../../aspose.words/font/doublestrikethrough/) { get; set; } | صحيح إذا تم تنسيق الخط كنص مزدوج الشطب. |
| [Emboss](../../aspose.words/font/emboss/) { get; set; } | صحيح إذا تم تنسيق الخط على أنه منقوش. |
| [EmphasisMark](../../aspose.words/font/emphasismark/) { get; set; } | يحصل على علامة التأكيد المطبقة على هذا التنسيق أو يعينها. |
| [Engrave](../../aspose.words/font/engrave/) { get; set; } | صحيح إذا تم تنسيق الخط على أنه محفور. |
| [Fill](../../aspose.words/font/fill/) { get; } | يحصل على تنسيق التعبئة لـ`Font` . |
| [Hidden](../../aspose.words/font/hidden/) { get; set; } | صحيح إذا تم تنسيق الخط كنص مخفي. |
| [HighlightColor](../../aspose.words/font/highlightcolor/) { get; set; } | يحصل على لون التمييز (العلامة) أو يعينه. |
| [Italic](../../aspose.words/font/italic/) { get; set; } | صحيح إذا تم تنسيق الخط على أنه مائل. |
| [ItalicBi](../../aspose.words/font/italicbi/) { get; set; } | صحيح إذا تم تنسيق النص من اليمين إلى اليسار بالخط المائل. |
| [Kerning](../../aspose.words/font/kerning/) { get; set; } | يحصل على حجم الخط الذي يبدأ عنده التباعد بين الأحرف أو يعينه. |
| [LineSpacing](../../aspose.words/font/linespacing/) { get; } | إرجاع المسافة بين أسطر هذا الخط (بالنقاط). |
| [LocaleId](../../aspose.words/font/localeid/) { get; set; } | يحصل على معرف الإعدادات المحلية (اللغة) للأحرف المنسقة أو يعينه. |
| [LocaleIdBi](../../aspose.words/font/localeidbi/) { get; set; } | يحصل على معرف الإعدادات المحلية (اللغة) للأحرف المنسقة من اليمين إلى اليسار أو يعينه. |
| [LocaleIdFarEast](../../aspose.words/font/localeidfareast/) { get; set; } | يحصل على معرف الإعدادات المحلية (اللغة) للأحرف الآسيوية المنسقة أو يعينه. |
| [Name](../../aspose.words/font/name/) { get; set; } | يحصل على اسم الخط أو يعينه. |
| [NameAscii](../../aspose.words/font/nameascii/) { get; set; } | يعيد أو يضبط الخط المستخدم للنص اللاتيني (الأحرف التي تحتوي على رموز أحرف من 0 (صفر) إلى 127). |
| [NameBi](../../aspose.words/font/namebi/) { get; set; } | يقوم بإرجاع أو تعيين اسم الخط في مستند لغة من اليمين إلى اليسار. |
| [NameFarEast](../../aspose.words/font/namefareast/) { get; set; } | يعيد أو يعين اسم الخط الآسيوي الشرقي. |
| [NameOther](../../aspose.words/font/nameother/) { get; set; } | يعيد أو يضبط الخط المستخدم للأحرف التي تحتوي على رموز أحرف من 128 إلى 255. |
| [NoProofing](../../aspose.words/font/noproofing/) { get; set; } | صحيح عندما لا يتم التحقق من صحة الأحرف المنسقة. |
| [NumberSpacing](../../aspose.words/font/numberspacing/) { get; set; } | يحصل على نوع المسافة للرقم الذي يتم عرضه أو يعينه. |
| [Outline](../../aspose.words/font/outline/) { get; set; } | صحيح إذا تم تنسيق الخط كمخطط تفصيلي. |
| [Position](../../aspose.words/font/position/) { get; set; } | يحصل على موضع النص (بالنقاط) أو يعينه بالنسبة لسطر الأساس. يرفع الرقم الموجب النص، ويخفضه الرقم السالب. |
| [Scaling](../../aspose.words/font/scaling/) { get; set; } | يحصل على مقياس عرض الحرف كنسبة مئوية أو يعينه. |
| [Shading](../../aspose.words/font/shading/) { get; } | يعيد[`Shading`](../shading/) كائن يشير إلى تنسيق التظليل للخط. |
| [Shadow](../../aspose.words/font/shadow/) { get; set; } | صحيح إذا تم تنسيق الخط على أنه مظلل. |
| [Size](../../aspose.words/font/size/) { get; set; } | يحصل على حجم الخط بالنقاط أو يعينه. |
| [SizeBi](../../aspose.words/font/sizebi/) { get; set; } | يحصل على حجم الخط بالنقاط المستخدمة في مستند من اليمين إلى اليسار أو يعينه. |
| [SmallCaps](../../aspose.words/font/smallcaps/) { get; set; } | صحيح إذا تم تنسيق الخط بأحرف كبيرة صغيرة. |
| [SnapToGrid](../../aspose.words/font/snaptogrid/) { get; set; } | يحدد ما إذا كان الخط الحالي يجب أن يستخدم إعدادات شبكة المستند للأحرف لكل سطر عند التخطيط. |
| [Spacing](../../aspose.words/font/spacing/) { get; set; } | يعيد أو يضبط المسافة (بالنقاط) بين الأحرف. |
| [StrikeThrough](../../aspose.words/font/strikethrough/) { get; set; } | صحيح إذا تم تنسيق الخط كنص مشطوب. |
| [Style](../../aspose.words/font/style/) { get; set; } | يحصل على نمط الحرف المطبق على هذا التنسيق أو يعينه. |
| [StyleIdentifier](../../aspose.words/font/styleidentifier/) { get; set; } | يحصل على أو يعين معرف النمط المستقل عن الإعدادات المحلية لنمط الأحرف المطبق على هذا التنسيق. |
| [StyleName](../../aspose.words/font/stylename/) { get; set; } | يحصل على اسم نمط الحرف المطبق على هذا التنسيق أو يعينه. |
| [Subscript](../../aspose.words/font/subscript/) { get; set; } | صحيح إذا تم تنسيق الخط على شكل خط منخفض. |
| [Superscript](../../aspose.words/font/superscript/) { get; set; } | صحيح إذا تم تنسيق الخط كخط علوي. |
| [TextEffect](../../aspose.words/font/texteffect/) { get; set; } | يحصل على تأثير الرسوم المتحركة للخط أو يعينه. |
| [ThemeColor](../../aspose.words/font/themecolor/) { get; set; } | يحصل على لون السمة أو يعينه في مخطط الألوان المطبق المرتبط بهذا`Font` الكائن. |
| [ThemeFont](../../aspose.words/font/themefont/) { get; set; } | يحصل على خط السمة أو يعينه في مخطط الخطوط المطبق المرتبط بهذا`Font` الكائن. |
| [ThemeFontAscii](../../aspose.words/font/themefontascii/) { get; set; } | يحصل على أو يعين الخط الموضوعي المستخدم للنص اللاتيني (الأحرف ذات رموز الأحرف من 0 (صفر) إلى 127) في مخطط الخط المطبق المرتبط بهذا`Font` الكائن. |
| [ThemeFontBi](../../aspose.words/font/themefontbi/) { get; set; } | يحصل على خط السمة أو يعينه في مخطط الخطوط المطبق المرتبط بهذا`Font` object في مستند بلغة من اليمين إلى اليسار. |
| [ThemeFontFarEast](../../aspose.words/font/themefontfareast/) { get; set; } | يحصل على أو يعين خط السمة الآسيوية الشرقية في مخطط الخطوط المطبق المرتبط بهذا`Font` الكائن. |
| [ThemeFontOther](../../aspose.words/font/themefontother/) { get; set; } | يحصل على أو يعين خط السمة المستخدم للأحرف التي تحتوي على رموز أحرف من 128 إلى 255 في مخطط الخط المطبق المرتبط بهذا`Font` الكائن. |
| [TintAndShade](../../aspose.words/font/tintandshade/) { get; set; } | يحصل على قيمة مزدوجة لتفتيح اللون أو تعتيمه أو تعيينها. |
| [Underline](../../aspose.words/font/underline/) { get; set; } | يحصل على نوع الخط السفلي المطبق على الخط أو يعينه. |
| [UnderlineColor](../../aspose.words/font/underlinecolor/) { get; set; } | يحصل على لون الخط السفلي المطبق على الخط أو يعينه. |

## طُرق

| اسم | وصف |
| --- | --- |
| [ClearFormatting](../../aspose.words/font/clearformatting/)() | إعادة التعيين إلى تنسيق الخط الافتراضي. |
| [HasDmlEffect](../../aspose.words/font/hasdmleffect/)(*[TextDmlEffect](../textdmleffect/)*) | يتحقق مما إذا كان يتم تطبيق تأثير نص DrawingML معين. |

## ملاحظات

لا تقم بإنشاء حالات من`Font` الصف مباشرةً. ما عليك سوى استخدام `Font` للوصول إلى خصائص الخط الخاصة بالأشياء المختلفة مثل[`Run`](../run/) ، [`Paragraph`](../paragraph/) ،[`Style`](../style/) ،[`DocumentBuilder`](../documentbuilder/).

## أمثلة

يوضح كيفية تنسيق سلسلة من النص باستخدام خاصية الخط الخاصة به.

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

يوضح كيفية إدراج سلسلة محاطة بحدود في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

يوضح كيفية إنشاء نمط الفقرة واستخدامه مع تنسيق القائمة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إنشاء نمط فقرة مخصص.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// قم بإنشاء قائمة وتأكد من أن الفقرات التي تستخدم هذا النمط سوف تستخدم هذه القائمة.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// قم بتطبيق نمط الفقرة على الفقرة الحالية في منشئ المستند، ثم أضف بعض النص.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// قم بتغيير نمط منشئ المستندات إلى نمط لا يحتوي على تنسيق القائمة واكتب فقرة أخرى.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
