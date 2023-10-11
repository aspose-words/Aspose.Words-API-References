---
title: Class ListFormat
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Lists.ListFormat فصل. يسمح بالتحكم في تنسيق القائمة المطبق على الفقرة.
type: docs
weight: 3480
url: /ar/net/aspose.words.lists/listformat/
---
## ListFormat class

يسمح بالتحكم في تنسيق القائمة المطبق على الفقرة.

لمعرفة المزيد، قم بزيارة[العمل مع القوائم](https://docs.aspose.com/words/net/working-with-lists/) مقالة توثيقية.

```csharp
public class ListFormat
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [IsListItem](../../aspose.words.lists/listformat/islistitem/) { get; } | صحيح عندما يتم تطبيق التنسيق النقطي أو الرقمي على الفقرة. |
| [List](../../aspose.words.lists/listformat/list/) { get; set; } | الحصول على القائمة التي تنتمي إليها هذه الفقرة أو تعيينها. |
| [ListLevel](../../aspose.words.lists/listformat/listlevel/) { get; } | إرجاع التنسيق على مستوى القائمة بالإضافة إلى أي تجاوزات تنسيق مطبقة على الفقرة الحالية. |
| [ListLevelNumber](../../aspose.words.lists/listformat/listlevelnumber/) { get; set; } | الحصول على أو تعيين رقم مستوى القائمة (0 إلى 8) للفقرة. |

## طُرق

| اسم | وصف |
| --- | --- |
| [ApplyBulletDefault](../../aspose.words.lists/listformat/applybulletdefault/)() | يبدأ قائمة نقطية افتراضية جديدة ويطبقها على الفقرة. |
| [ApplyNumberDefault](../../aspose.words.lists/listformat/applynumberdefault/)() | بدء قائمة مرقمة افتراضية جديدة وتطبيقها على الفقرة. |
| [ListIndent](../../aspose.words.lists/listformat/listindent/)() | زيادة مستوى القائمة للفقرة الحالية بمقدار مستوى واحد. |
| [ListOutdent](../../aspose.words.lists/listformat/listoutdent/)() | تقليل مستوى القائمة للفقرة الحالية بمقدار مستوى واحد. |
| [RemoveNumbers](../../aspose.words.lists/listformat/removenumbers/)() | إزالة الأرقام أو التعداد النقطي من الفقرة الحالية وتعيين مستوى القائمة إلى صفر. |

### ملاحظات

يمكن تعداد فقرة في مستند Microsoft Word أو تعدادها. عندما يتم تعداد فقرة أو تعدادها، يقال أنه يتم تطبيق تنسيق القائمة على الفقرة.

لا تقم بإنشاء كائنات من`ListFormat` الفصل مباشرة. يمكنك الوصول`ListFormat` كخاصية لكائن آخر يمكن أن يكون له تنسيق قائمة مرتبط به. في الوقت الحالي، الكائنات التي يمكن أن يكون لها تنسيق قائمة هي:[`Paragraph`](../../aspose.words/paragraph/)[`Style`](../../aspose.words/style/) و[`DocumentBuilder`](../../aspose.words/documentbuilder/).

`ListFormat` من أ[`Paragraph`](../../aspose.words/paragraph/) يحدد ما هو تنسيق القائمة ومستوى القائمة المطبق على تلك الفقرة المحددة.

`ListFormat` من أ[`Style`](../../aspose.words/style/) (applicable على أنماط الفقرة فقط) يسمح بتحديد تنسيق القائمة وlevel الذي يتم تطبيقه على جميع الفقرات بهذا النمط المعين.

`ListFormat` من أ[`DocumentBuilder`](../../aspose.words/documentbuilder/) يوفر الوصول إلى تنسيق القائمة في موضع المؤشر الحالي داخل[`DocumentBuilder`](../../aspose.words/documentbuilder/).

يتم تخزين تنسيق القائمة نفسه داخل ملف[`List`](../list/) كائن الذي يتم تخزينه بشكل منفصل عن الفقرات. يتم تخزين قائمة الكائنات داخل ملف[`ListCollection`](../listcollection/) مجموعة. هناك واحد [`ListCollection`](../listcollection/) جمع لكل[`Document`](../../aspose.words/document/).

الفقرات لا تنتمي فعليًا إلى القائمة. تشير الفقرات just إلى كائن قائمة معين عبر ملف[`List`](./list/) property ومستوى معين في القائمة عبر[`ListLevelNumber`](./listlevelnumber/) property. من خلال تعيين هاتين الخاصيتين، يمكنك التحكم في التعداد النقطي والترقيم الذي سيتم تطبيقه على الفقرة.

### أمثلة

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


