---
title: Class ListLevel
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Lists.ListLevel فصل. يحدد التنسيق لمستوى القائمة .
type: docs
weight: 3300
url: /ar/net/aspose.words.lists/listlevel/
---
## ListLevel class

يحدد التنسيق لمستوى القائمة .

```csharp
public class ListLevel
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Alignment](../../aspose.words.lists/listlevel/alignment/) { get; set; } | الحصول على أو تحديد تبرير العدد الفعلي لعنصر القائمة. |
| [CustomNumberStyleFormat](../../aspose.words.lists/listlevel/customnumberstyleformat/) { get; } | الحصول على تنسيق نمط الرقم المخصص لمستوى القائمة هذا. على سبيل المثال: "a، ç، ĝ، ..." . |
| [Font](../../aspose.words.lists/listlevel/font/) { get; } | تحديد تنسيق الأحرف المستخدم لتسمية القائمة. |
| [ImageData](../../aspose.words.lists/listlevel/imagedata/) { get; } | إرجاع بيانات الصورة لشكل التعداد النقطي للصورة لمستوى القائمة الحالي. |
| [IsLegal](../../aspose.words.lists/listlevel/islegal/) { get; set; } | صحيح إذا قام المستوى بتحويل جميع الأرقام الموروثة إلى اللغة العربية ، خطأ إذا احتفظ بنمط الأرقام . |
| [LinkedStyle](../../aspose.words.lists/listlevel/linkedstyle/) { get; set; } | الحصول على أو تحديد نمط الفقرة المرتبط بمستوى القائمة هذا. |
| [NumberFormat](../../aspose.words.lists/listlevel/numberformat/) { get; set; } | إرجاع أو تحديد تنسيق الأرقام لمستوى القائمة. |
| [NumberPosition](../../aspose.words.lists/listlevel/numberposition/) { get; set; } | إرجاع أو تعيين موضع الرقم أو الرمز النقطي لمستوى القائمة (بالنقاط). |
| [NumberStyle](../../aspose.words.lists/listlevel/numberstyle/) { get; set; } | إرجاع أو تحديد نمط الرقم لمستوى القائمة. |
| [RestartAfterLevel](../../aspose.words.lists/listlevel/restartafterlevel/) { get; set; } | تعيين أو إرجاع مستوى القائمة الذي يجب أن يظهر قبل أن يقوم مستوى القائمة المحدد بإعادة تشغيل الترقيم. |
| [StartAt](../../aspose.words.lists/listlevel/startat/) { get; set; } | إرجاع أو تحديد رقم البداية لمستوى القائمة هذا. |
| [TabPosition](../../aspose.words.lists/listlevel/tabposition/) { get; set; } | إرجاع أو تعيين موضع علامة التبويب (بالنقاط) لمستوى القائمة. |
| [TextPosition](../../aspose.words.lists/listlevel/textposition/) { get; set; } | إرجاع أو تعيين الموضع (بالنقاط) للسطر الثاني من التفاف النص لمستوى القائمة. |
| [TrailingCharacter](../../aspose.words.lists/listlevel/trailingcharacter/) { get; set; } | إرجاع أو تعيين الحرف الذي تم إدخاله بعد الرقم الخاص بمستوى القائمة. |

## طُرق

| اسم | وصف |
| --- | --- |
| [CreatePictureBullet](../../aspose.words.lists/listlevel/createpicturebullet/)() | إنشاء شكل تعداد نقطي للصورة لمستوى القائمة الحالية. |
| [DeletePictureBullet](../../aspose.words.lists/listlevel/deletepicturebullet/)() | حذف رمز نقطي للصورة لمستوى القائمة الحالية. |
| [Equals](../../aspose.words.lists/listlevel/equals/#equals)(ListLevel) | يقارن مع مستوى القائمة المحدد . |
| override [GetHashCode](../../aspose.words.lists/listlevel/gethashcode/)() | حساب كود التجزئة لهذا الكائن. |
| static [GetEffectiveValue](../../aspose.words.lists/listlevel/geteffectivevalue/)(int, NumberStyle, string) | يبين تمثيل السلسلة لملف`ListLevel` كائن index المحدد لعنصر القائمة. تحدد المعلمات ملف[`NumberStyle`](../../aspose.words/numberstyle/) وتنسيق اختياري string يتم استخدامه عندCustom محدد . |

### ملاحظات

لا تقوم بإنشاء كائنات من هذه الفئة. يتم إنشاء كائنات مستوى القائمة تلقائيًا عند إنشاء قائمة. يمكنك الوصول`ListLevel` الكائنات عبر the [`ListLevelCollection`](../listlevelcollection/) مجموعة.

استخدم خصائص`ListLevel` لتحديد تنسيق القائمة لمستويات القائمة الفردية.

### أمثلة

يوضح كيفية تطبيق تنسيق قائمة مخصص على الفقرات عند استخدام DocumentBuilder.

```csharp
Document doc = new Document();

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات برموز بادئة ومسافات بادئة.
// يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة. 
// يمكننا بدء قائمة وإنهائها باستخدام خاصية "تنسيق القائمة" الخاصة بمنشئ المستندات. 
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// إنشاء قائمة من قالب Microsoft Word ، وتخصيص أول مستويين من القائمة.
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

// ستنشئ قيمة NumberFormat هذه رموز قائمة ذات تعداد نقطي على شكل نجمة.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// أنشئ فقرات وقم بتطبيق كلا مستويي القائمة لتنسيق قائمتنا المخصص عليها.
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


