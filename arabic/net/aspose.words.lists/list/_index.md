---
title: Class List
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Lists.List فصل. يمثل تنسيق القائمة.
type: docs
weight: 3460
url: /ar/net/aspose.words.lists/list/
---
## List class

يمثل تنسيق القائمة.

لمعرفة المزيد، قم بزيارة[العمل مع القوائم](https://docs.aspose.com/words/net/working-with-lists/) مقالة توثيقية.

```csharp
public class List : IComparable<List>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Document](../../aspose.words.lists/list/document/) { get; } | الحصول على مستند المالك. |
| [IsListStyleDefinition](../../aspose.words.lists/list/isliststyledefinition/) { get; } | إرجاع`حقيقي` إذا كانت هذه القائمة عبارة عن تعريف لنمط القائمة. |
| [IsListStyleReference](../../aspose.words.lists/list/isliststylereference/) { get; } | إرجاع`حقيقي` إذا كانت هذه القائمة مرجعًا لنمط القائمة. |
| [IsMultiLevel](../../aspose.words.lists/list/ismultilevel/) { get; } | إرجاع`حقيقي` عندما تحتوي القائمة على 9 مستويات؛`خطأ شنيع` عندما يكون المستوى 1. |
| [IsRestartAtEachSection](../../aspose.words.lists/list/isrestartateachsection/) { get; set; } | يحدد ما إذا كان يجب إعادة تشغيل القائمة في كل قسم. القيمة الافتراضية هي`خطأ شنيع` . |
| [ListId](../../aspose.words.lists/list/listid/) { get; } | الحصول على المعرف الفريد للقائمة. |
| [ListLevels](../../aspose.words.lists/list/listlevels/) { get; } | الحصول على مجموعة مستويات القائمة لهذه القائمة. |
| [Style](../../aspose.words.lists/list/style/) { get; } | الحصول على نمط القائمة الذي تشير إليه هذه القائمة أو تحدده. |

## طُرق

| اسم | وصف |
| --- | --- |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto)(List) | مقارنة القائمة المحددة بالقائمة الحالية. |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto_1)(object) | مقارنة الكائن المحدد بالكائن الحالي. |
| [Equals](../../aspose.words.lists/list/equals/#equals)(List) | يقارن بالقائمة المحددة. |
| override [Equals](../../aspose.words.lists/list/equals/#equals_1)(object) | تحديد ما إذا كان الكائن المحدد يساوي قيمة الكائن الحالي. |
| override [GetHashCode](../../aspose.words.lists/list/gethashcode/)() | لحساب رمز التجزئة لكائن القائمة هذا. |
| [HasSameTemplate](../../aspose.words.lists/list/hassametemplate/)(List) | إرجاع صحيح إذا تم إنشاء القائمة الحالية والقائمة المحددة من نفس القالب. |

### ملاحظات

القائمة في مستند Microsoft Word عبارة عن مجموعة من خصائص تنسيق القائمة. يمكن أن تحتوي كل قائمة على ما يصل إلى 9 مستويات ويتم تحديد خصائص التنسيق، مثل نمط الرقم، وقيمة البداية، و المسافة البادئة، وموضع علامة التبويب وما إلى ذلك بشكل منفصل لكل مستوى.

أ`List` الكائن ينتمي دائمًا إلى[`ListCollection`](../listcollection/) مجموعة.

لإنشاء قائمة جديدة، استخدم أساليب الإضافة الخاصة بـ[`ListCollection`](../listcollection/) مجموعة.

لتعديل تنسيق القائمة، استخدم[`ListLevel`](../listlevel/) الكائنات التي تم العثور عليها في [`ListLevels`](./listlevels/) مجموعة.

لتطبيق تنسيق القائمة أو إزالته من فقرة، استخدم[`ListFormat`](../listformat/).

### أمثلة

يوضح كيفية إعادة تشغيل الترقيم في القائمة عن طريق نسخ القائمة.

```csharp
Document doc = new Document();

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات برموز البادئة والمسافات البادئة.
 // يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة.
 // يمكننا بدء القائمة وإنهائها باستخدام خاصية "ListFormat" الخاصة بمنشئ المستندات.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// قم بإنشاء قائمة من قالب Microsoft Word، وقم بتخصيص مستوى القائمة الأول الخاص بها.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// قم بتطبيق قائمتنا على بعض الفقرات.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// يمكننا إضافة نسخة من القائمة الموجودة إلى مجموعة قائمة الوثيقة
// لإنشاء قائمة مماثلة دون إجراء تغييرات على القائمة الأصلية.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// قم بتطبيق القائمة الثانية على فقرات جديدة.
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

يوضح كيفية تطبيق تنسيق القائمة المخصصة على الفقرات عند استخدام DocumentBuilder.

```csharp
Document doc = new Document();

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات برموز البادئة والمسافات البادئة.
 // يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة.
 // يمكننا بدء القائمة وإنهائها باستخدام خاصية "ListFormat" الخاصة بمنشئ المستندات.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// أنشئ قائمة من قالب Microsoft Word، وقم بتخصيص المستويين الأولين من قائمتها.
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

// ستعمل قيمة NumberFormat هذه على إنشاء رموز قائمة نقطية على شكل نجمة.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// قم بإنشاء فقرات وتطبيق كلا مستويي القائمة بتنسيق القائمة المخصص لدينا عليها.
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

يوضح كيفية العمل مع مستويات القائمة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات برموز البادئة والمسافات البادئة.
 // يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة.
 // يمكننا بدء القائمة وإنهائها باستخدام خاصية "ListFormat" الخاصة بمنشئ المستندات.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// فيما يلي نوعان من القوائم التي يمكننا إنشاؤها باستخدام أداة إنشاء المستندات.
// 1 - قائمة مرقمة:
// تنشئ القوائم المرقمة ترتيبًا منطقيًا لفقراتها عن طريق ترقيم كل عنصر.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// من خلال تعيين خاصية "ListLevelNumber"، يمكننا زيادة مستوى القائمة
// لبدء قائمة فرعية قائمة بذاتها في عنصر القائمة الحالي.
// يستخدم قالب قائمة Microsoft Word المسمى "NumberDefault" الأرقام لإنشاء مستويات القائمة لمستوى القائمة الأول.
 // تستخدم مستويات القائمة الأعمق الحروف والأرقام الرومانية الصغيرة.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - قائمة ذات تعداد نقطي:
// ستطبق هذه القائمة مسافة بادئة ورمز نقطي ("•") قبل كل فقرة.
// ستستخدم المستويات الأعمق لهذه القائمة رموزًا مختلفة، مثل "■" و"○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// يمكننا تعطيل تنسيق القائمة لعدم تنسيق أي فقرات لاحقة كقوائم عن طريق إلغاء تعيين علامة "القائمة".
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Lists](../../aspose.words.lists/)
* المجسم [Aspose.Words](../../)


