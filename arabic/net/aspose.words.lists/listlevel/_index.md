---
title: ListLevel Class
linktitle: ListLevel
articleTitle: ListLevel
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Lists.ListLevel لتنسيق القوائم المتقدم. حسّن بنية مستندك بخيارات فعّالة وقابلة للتخصيص.
type: docs
weight: 3950
url: /ar/net/aspose.words.lists/listlevel/
---
## ListLevel class

يحدد التنسيق لمستوى القائمة.

لمعرفة المزيد، قم بزيارة[العمل مع القوائم](https://docs.aspose.com/words/net/working-with-lists/) مقالة توثيقية.

```csharp
public class ListLevel
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Alignment](../../aspose.words.lists/listlevel/alignment/) { get; set; } | يحصل على مبرر العدد الفعلي لعنصر القائمة أو يعينه. |
| [CustomNumberStyleFormat](../../aspose.words.lists/listlevel/customnumberstyleformat/) { get; set; } | يحصل على أو يضبط تنسيق نمط الأرقام المخصص لمستوى القائمة هذا. على سبيل المثال: "a, ç, ĝ, ...". |
| [Font](../../aspose.words.lists/listlevel/font/) { get; } | يحدد تنسيق الأحرف المستخدم لتسمية القائمة. |
| [ImageData](../../aspose.words.lists/listlevel/imagedata/) { get; } | إرجاع بيانات الصورة لشكل النقطة للصورة لمستوى القائمة الحالي. |
| [IsLegal](../../aspose.words.lists/listlevel/islegal/) { get; set; } | صحيح إذا قام المستوى بتحويل جميع الأرقام الموروثة إلى اللغة العربية، خطأ إذا حافظ على نمط أرقامها. |
| [LinkedStyle](../../aspose.words.lists/listlevel/linkedstyle/) { get; set; } | يحصل على نمط الفقرة المرتبط بمستوى القائمة هذا أو يعينه. |
| [NumberFormat](../../aspose.words.lists/listlevel/numberformat/) { get; set; } | يعيد أو يعين تنسيق الرقم لمستوى القائمة. |
| [NumberPosition](../../aspose.words.lists/listlevel/numberposition/) { get; set; } | يعيد أو يعين موضع (بالنقاط) الرقم أو النقطة لمستوى القائمة. |
| [NumberStyle](../../aspose.words.lists/listlevel/numberstyle/) { get; set; } | يعيد أو يعين نمط الرقم لمستوى القائمة هذا. |
| [RestartAfterLevel](../../aspose.words.lists/listlevel/restartafterlevel/) { get; set; } | تعيين أو إرجاع مستوى القائمة الذي يجب أن يظهر قبل إعادة تشغيل الترقيم بمستوى القائمة المحدد. |
| [StartAt](../../aspose.words.lists/listlevel/startat/) { get; set; } | يعيد أو يعين الرقم الابتدائي لمستوى القائمة هذا. |
| [TabPosition](../../aspose.words.lists/listlevel/tabposition/) { get; set; } | يعيد أو يعين موضع علامة التبويب (بالنقاط) لمستوى القائمة. |
| [TextPosition](../../aspose.words.lists/listlevel/textposition/) { get; set; } | يعيد أو يعين الموضع (بالنقاط) للسطر الثاني من النص الملتف لمستوى القائمة. |
| [TrailingCharacter](../../aspose.words.lists/listlevel/trailingcharacter/) { get; set; } | يعيد أو يعين الحرف الذي تم إدراجه بعد الرقم لمستوى القائمة. |

## طُرق

| اسم | وصف |
| --- | --- |
| [CreatePictureBullet](../../aspose.words.lists/listlevel/createpicturebullet/)() | ينشئ شكل نقطي للصورة لمستوى القائمة الحالي. |
| [DeletePictureBullet](../../aspose.words.lists/listlevel/deletepicturebullet/)() | يحذف صورة النقطة لمستوى القائمة الحالي. |
| [Equals](../../aspose.words.lists/listlevel/equals/#equals)(*ListLevel*) | يقارن مع ListLevel المحدد. |
| override [GetHashCode](../../aspose.words.lists/listlevel/gethashcode/)() | يحسب رمز التجزئة لهذا الكائن. |
| static [GetEffectiveValue](../../aspose.words.lists/listlevel/geteffectivevalue/)(*int, [NumberStyle](../../aspose.words/numberstyle/), string*) | يعرض التمثيل النصي لـ`ListLevel`كائن لـ index المحدد لعنصر القائمة. تحدد المعلمات[`NumberStyle`](../../aspose.words/numberstyle/) وتنسيق اختياري string يستخدم عندCustom تم تحديده. |

## ملاحظات

لا تُنشئ كائنات من هذه الفئة. تُنشأ كائنات مستوى القائمة تلقائيًا عند إنشاء قائمة. يمكنك الوصول إلى`ListLevel` الكائنات عبر the [`ListLevelCollection`](../listlevelcollection/) مجموعة.

استخدم خصائص`ListLevel` لتحديد تنسيق القائمة لمستويات القائمة الفردية.

## أمثلة

يوضح كيفية تطبيق تنسيق القائمة المخصصة على الفقرات عند استخدام DocumentBuilder.

```csharp
Document doc = new Document();

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات باستخدام رموز البادئة والمسافات البادئة.
 //يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة.
 // يمكننا أن نبدأ وننهي القائمة باستخدام خاصية "ListFormat" الموجودة في منشئ المستندات.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// قم بإنشاء قائمة من قالب Microsoft Word، ثم قم بتخصيص المستويين الأولين من القائمة.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// ستقوم قيمة NumberFormat هذه بإنشاء رموز قائمة نقطية على شكل نجمة.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// قم بإنشاء فقرات ثم قم بتطبيق مستويي القائمة لتنسيق القائمة المخصصة عليها.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Lists](../../aspose.words.lists/)
* المجسم [Aspose.Words](../../)
