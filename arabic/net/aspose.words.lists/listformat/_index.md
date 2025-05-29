---
title: ListFormat Class
linktitle: ListFormat
articleTitle: ListFormat
second_title: Aspose.Words لـ .NET
description: تنسيق القوائم الرئيسية في مستنداتك باستخدام فئة Aspose.Words.Lists.ListFormat. حسّن تنسيق الفقرات بسهولة لتحسين قابلية القراءة.
type: docs
weight: 3930
url: /ar/net/aspose.words.lists/listformat/
---
## ListFormat class

يسمح بالتحكم في تنسيق القائمة المطبق على فقرة.

لمعرفة المزيد، قم بزيارة[العمل مع القوائم](https://docs.aspose.com/words/net/working-with-lists/) مقالة توثيقية.

```csharp
public class ListFormat
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [IsListItem](../../aspose.words.lists/listformat/islistitem/) { get; } | صحيح عندما يتم تطبيق تنسيق نقطي أو رقمي على الفقرة. |
| [List](../../aspose.words.lists/listformat/list/) { get; set; } | يحصل على القائمة التي تكون هذه الفقرة عضوًا فيها أو يعينها. |
| [ListLevel](../../aspose.words.lists/listformat/listlevel/) { get; } | يعيد تنسيق مستوى القائمة بالإضافة إلى أي تجاوزات تنسيق يتم تطبيقها على الفقرة الحالية. |
| [ListLevelNumber](../../aspose.words.lists/listformat/listlevelnumber/) { get; set; } | يحصل على رقم مستوى القائمة (من 0 إلى 8) للفقرة أو يعينه. |

## طُرق

| اسم | وصف |
| --- | --- |
| [ApplyBulletDefault](../../aspose.words.lists/listformat/applybulletdefault/)() | يبدأ قائمة نقطية افتراضية جديدة ويطبقها على الفقرة. |
| [ApplyNumberDefault](../../aspose.words.lists/listformat/applynumberdefault/)() | يبدأ قائمة مرقمة افتراضية جديدة ويطبقها على الفقرة. |
| [ListIndent](../../aspose.words.lists/listformat/listindent/)() | يزيد مستوى القائمة للفقرة الحالية بمستوى واحد. |
| [ListOutdent](../../aspose.words.lists/listformat/listoutdent/)() | يقلل مستوى القائمة للفقرة الحالية بمستوى واحد. |
| [RemoveNumbers](../../aspose.words.lists/listformat/removenumbers/)() | يزيل الأرقام أو النقاط من الفقرة الحالية ويضبط مستوى القائمة إلى الصفر. |

## ملاحظات

يمكن أن تكون الفقرة في مستند Microsoft Word نقطية أو مرقمة. عندما تكون الفقرة نقطية أو مرقمة، يقال أن تنسيق القائمة يتم تطبيقه على الفقرة.

لا تقم بإنشاء كائنات من`ListFormat` الصف مباشرة. يمكنك الوصول إليه`ListFormat`كخاصية لكائن آخر يُمكنه استخدام تنسيق قائمة مع x000d_. حاليًا، الكائنات التي يُمكنه استخدام تنسيق قائمة مع x000d_ هي:[`Paragraph`](../../aspose.words/paragraph/) ، [`Style`](../../aspose.words/style/) و[`DocumentBuilder`](../../aspose.words/documentbuilder/).

`ListFormat` من أ[`Paragraph`](../../aspose.words/paragraph/) يحدد تنسيق القائمة ومستوى القائمة المطبق على تلك الفقرة المعينة.

`ListFormat` من أ[`Style`](../../aspose.words/style/) (applicable على أنماط الفقرات فقط) يسمح بتحديد تنسيق القائمة ومستوى القائمة الذي يتم تطبيقه على جميع فقرات هذا النمط المعين.

`ListFormat` من أ[`DocumentBuilder`](../../aspose.words/documentbuilder/) يوفر إمكانية الوصول إلى تنسيق القائمة في موضع المؤشر الحالي داخل[`DocumentBuilder`](../../aspose.words/documentbuilder/).

يتم تخزين تنسيق القائمة نفسها داخل[`List`](../list/) كائن مُخزَّن بشكل منفصل عن الفقرات. تُخزَّن قائمة الكائنات داخل[`ListCollection`](../listcollection/) مجموعة. يوجد single [`ListCollection`](../listcollection/) المجموعة لكل[`Document`](../../aspose.words/document/).

الفقرات لا تنتمي فعليًا إلى قائمة. الفقرات just تُشير إلى كائن قائمة مُحدد عبر[`List`](./list/) property ومستوى معين في القائمة عبر[`ListLevelNumber`](./listlevelnumber/) property. من خلال تعيين هاتين الخاصيتين، يمكنك التحكم في النقاط والأرقام التي يتم تطبيقها على فقرة.

## أمثلة

يوضح كيفية العمل مع مستويات القائمة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات باستخدام رموز البادئة والمسافات البادئة.
 //يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة.
 // يمكننا أن نبدأ وننهي القائمة باستخدام خاصية "ListFormat" الموجودة في منشئ المستندات.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// فيما يلي نوعان من القوائم التي يمكننا إنشاؤها باستخدام منشئ المستندات.
// 1 - قائمة مرقمة:
// تقوم القوائم المرقمة بإنشاء ترتيب منطقي لفقراتها عن طريق ترقيم كل عنصر.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// من خلال تعيين خاصية "ListLevelNumber"، يمكننا زيادة مستوى القائمة
// لبدء قائمة فرعية مستقلة عند عنصر القائمة الحالي.
// يستخدم قالب قائمة Microsoft Word المسمى "NumberDefault" الأرقام لإنشاء مستويات القائمة للمستوى الأول من القائمة.
 // تستخدم مستويات القائمة الأعمق الأحرف والأرقام الرومانية الصغيرة.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - قائمة نقطية:
// ستطبق هذه القائمة مسافة بادئة ورمز نقطي ("•") قبل كل فقرة.
// ستستخدم المستويات الأعمق من هذه القائمة رموزًا مختلفة، مثل "■" و"○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// يمكننا تعطيل تنسيق القائمة لعدم تنسيق أي فقرات لاحقة كقوائم عن طريق إلغاء تعيين علم "القائمة".
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Lists](../../aspose.words.lists/)
* المجسم [Aspose.Words](../../)
