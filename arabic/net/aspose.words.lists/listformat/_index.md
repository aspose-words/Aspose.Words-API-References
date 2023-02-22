---
title: Class ListFormat
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Lists.ListFormat فصل. يسمح بالتحكم في تنسيق القائمة المطبق على فقرة.
type: docs
weight: 3280
url: /ar/net/aspose.words.lists/listformat/
---
## ListFormat class

يسمح بالتحكم في تنسيق القائمة المطبق على فقرة.

```csharp
public class ListFormat
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [IsListItem](../../aspose.words.lists/listformat/islistitem/) { get; } | صحيح عندما يتم تطبيق تنسيق تعداد نقطي أو رقمي على الفقرة. |
| [List](../../aspose.words.lists/listformat/list/) { get; set; } | الحصول على أو تعيين القائمة التي تكون هذه الفقرة عضوًا فيها. |
| [ListLevel](../../aspose.words.lists/listformat/listlevel/) { get; } | إرجاع تنسيق مستوى القائمة بالإضافة إلى أي تجاوزات تنسيق مطبقة على الفقرة الحالية. |
| [ListLevelNumber](../../aspose.words.lists/listformat/listlevelnumber/) { get; set; } | الحصول على أو تحديد رقم مستوى القائمة (من 0 إلى 8) للفقرة. |

## طُرق

| اسم | وصف |
| --- | --- |
| [ApplyBulletDefault](../../aspose.words.lists/listformat/applybulletdefault/)() | يبدأ قائمة افتراضية جديدة ذات تعداد نقطي ويطبقها على الفقرة. |
| [ApplyNumberDefault](../../aspose.words.lists/listformat/applynumberdefault/)() | يبدأ قائمة مرقمة افتراضية جديدة ويطبقها على الفقرة. |
| [ListIndent](../../aspose.words.lists/listformat/listindent/)() | زيادة مستوى قائمة الفقرة الحالية بمقدار مستوى واحد. |
| [ListOutdent](../../aspose.words.lists/listformat/listoutdent/)() | تقليل مستوى قائمة الفقرة الحالية بمستوى واحد. |
| [RemoveNumbers](../../aspose.words.lists/listformat/removenumbers/)() | يزيل الأرقام أو الرموز النقطية من الفقرة الحالية ويضبط مستوى القائمة على صفر. |

### ملاحظات

يمكن أن تكون الفقرة في مستند Microsoft Word ذات تعداد نقطي أو رقمي.

لا تقوم بإنشاء كائنات من`ListFormat` فئة مباشرة. يمكنك الوصول إليها`ListFormat` كخاصية لكائن آخر يمكن أن يكون لها تنسيق قائمة مرتبط بها. في الوقت الحالي ، الكائنات التي يمكن أن يكون لها تنسيق قائمة هي:[`Paragraph`](../../aspose.words/paragraph/) ، [`Style`](../../aspose.words/style/) و[`DocumentBuilder`](../../aspose.words/documentbuilder/).

`ListFormat` من أ[`Paragraph`](../../aspose.words/paragraph/) specified ما هو تنسيق القائمة ومستوى القائمة المطبقين على تلك الفقرة المعينة.

`ListFormat` من أ[`Style`](../../aspose.words/style/)(ينطبق على أنماط الفقرة فقط) يسمح بتحديد تنسيق القائمة وقائمة المستوى المطبقة على جميع فقرات هذا النمط المعين.

`ListFormat` من أ[`DocumentBuilder`](../../aspose.words/documentbuilder/) يوفر الوصول إلى تنسيق القائمة في موضع المؤشر الحالي داخل ملف[`DocumentBuilder`](../../aspose.words/documentbuilder/).

يتم تخزين قائمة التنسيق نفسها داخل ملف[`List`](../list/) كائن مخزّن بشكل منفصل عن الفقرات. يتم تخزين كائنات القائمة داخل ملف[`ListCollection`](../listcollection/) مجموعة. هناك واحد [`ListCollection`](../listcollection/) جمع لكل[`Document`](../../aspose.words/document/).

لا تنتمي الفقرات فعليًا إلى قائمة. تشير الفقرات just إلى كائن قائمة معين عبر ملف[`List`](./list/) property ومستوى معين في القائمة عبر ملف[`ListLevelNumber`](./listlevelnumber/) property. من خلال تعيين هاتين الخاصيتين ، يمكنك التحكم في التعداد والترقيم الذي يتم تطبيقه على فقرة.

### أمثلة

يوضح كيفية العمل مع مستويات القائمة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات برموز بادئة ومسافات بادئة.
// يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة. 
// يمكننا بدء قائمة وإنهائها باستخدام خاصية "تنسيق القائمة" الخاصة بمنشئ المستندات. 
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// يوجد أدناه نوعان من القوائم التي يمكننا إنشاؤها باستخدام أداة إنشاء المستندات.
// 1 - قائمة ذات تعداد رقمي:
// تقوم القوائم المرقمة بإنشاء ترتيب منطقي لفقراتها عن طريق ترقيم كل عنصر.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// من خلال تعيين خاصية "ListLevelNumber" ، يمكننا زيادة مستوى القائمة
// لبدء قائمة فرعية قائمة بذاتها في عنصر القائمة الحالي.
// يستخدم قالب قائمة Microsoft Word المسمى "NumberDefault" الأرقام لإنشاء مستويات القائمة لمستوى القائمة الأول.
// تستخدم مستويات القائمة الأعمق أحرفًا وأرقامًا رومانية صغيرة. 
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - قائمة نقطية:
// ستطبق هذه القائمة مسافة بادئة ورمز نقطي ("•") قبل كل فقرة.
// ستستخدم المستويات الأعمق من هذه القائمة رموزًا مختلفة ، مثل "■" و "".
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


