---
title: ListCollection Class
linktitle: ListCollection
articleTitle: ListCollection
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Lists.ListCollection لإدارة فعالة للقوائم المرقمة والمنقطة، وتحسين تنسيق المستندات وتنظيمها.
type: docs
weight: 3920
url: /ar/net/aspose.words.lists/listcollection/
---
## ListCollection class

يخزن ويدير تنسيق القوائم المرقمة والمنقطة المستخدمة في المستند.

لمعرفة المزيد، قم بزيارة[العمل مع القوائم](https://docs.aspose.com/words/net/working-with-lists/) مقالة توثيقية.

```csharp
public class ListCollection : IEnumerable<List>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.lists/listcollection/count/) { get; } | يحصل على عدد القوائم المرقمة والمنقطة في المستند. |
| [Document](../../aspose.words.lists/listcollection/document/) { get; } | يحصل على مستند المالك. |
| [Item](../../aspose.words.lists/listcollection/item/) { get; } | يحصل على قائمة حسب الفهرس. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.lists/listcollection/add/#add)(*[ListTemplate](../listtemplate/)*) | ينشئ قائمة جديدة استنادًا إلى قالب محدد مسبقًا ويضيفها إلى مجموعة القوائم في المستند. |
| [Add](../../aspose.words.lists/listcollection/add/#add_1)(*[Style](../../aspose.words/style/)*) | ينشئ قائمة جديدة تشير إلى نمط القائمة ويضيفها إلى مجموعة القوائم في المستند. |
| [AddCopy](../../aspose.words.lists/listcollection/addcopy/)(*[List](../list/)*) | ينشئ قائمة جديدة عن طريق نسخ القائمة المحددة وإضافتها إلى مجموعة القوائم في المستند. |
| [AddSingleLevelList](../../aspose.words.lists/listcollection/addsinglelevellist/)(*[ListTemplate](../listtemplate/)*) | ينشئ قائمة جديدة ذات مستوى واحد استنادًا إلى القالب المحدد مسبقًا ويضيفها إلى مجموعة القوائم في المستند. |
| [GetEnumerator](../../aspose.words.lists/listcollection/getenumerator/)() | يحصل على كائن العد الذي سيقوم بإحصاء القوائم في المستند. |
| [GetListByListId](../../aspose.words.lists/listcollection/getlistbylistid/)(*int*) | يحصل على قائمة من خلال معرف القائمة. |

## ملاحظات

القائمة في مستند Microsoft Word عبارة عن مجموعة من خصائص تنسيق القائمة. يتم تخزين تنسيق القوائم في`ListCollection` مجموعة منفصلة عن فقرات النص.

لا تُنشئ كائنات من هذه الفئة. يوجد دائمًا كائن واحد فقط`ListCollection` كائن لكل مستند ويمكن الوصول إليه عبر[`Lists`](../../aspose.words/documentbase/lists/) ملكية.

لإنشاء قائمة جديدة استنادًا إلى قالب قائمة محدد مسبقًا أو استنادًا إلى نمط القائمة، استخدم [`Add`](./add/) طريقة.

لإنشاء قائمة جديدة بتنسيق مماثل لقائمة موجودة، استخدم [`AddCopy`](./addcopy/) طريقة.

لجعل الفقرة مرقمة أو منقطة، يجب عليك تطبيق قائمة formatting على الفقرة عن طريق تعيين[`List`](../list/)الاعتراض على [`List`](../listformat/list/) ممتلكات[`ListFormat`](../listformat/).

لإزالة تنسيق القائمة من فقرة، استخدم[`RemoveNumbers`](../listformat/removenumbers/) طريقة .

إذا كنتَ على درايةٍ بـ WordprocessingML، فربما تعلم أنه يُعرّف مفهومين منفصلين هما "القائمة" و"تعريف القائمة". يتوافق هذا تمامًا مع كيفية تخزين تنسيق القائمة في مستند Microsoft Word في المستوى الأدنى. تعريف القائمة أشبه بـ"مخطط"، وقائمة x000d هي مثالٌ لتعريف القائمة.

لتبسيط نموذج البرمجة، يخفي Aspose.Words التمييز بين القائمة وتعريف list بنفس الطريقة التي يخفيها Microsoft Word في واجهة المستخدم الخاصة به. يسمح لك هذا بالتركيز بشكل أكبر على الشكل الذي تريد أن يبدو عليه مستندك، بدلاً من بناء كائنات منخفضة المستوى لتلبية متطلبات تنسيق ملف Microsoft Word.

ليس من الممكن حذف القوائم بمجرد إنشائها في الإصدار الحالي من Aspose.Words. وهذا مشابه لبرنامج Microsoft Word حيث لا يتمتع المستخدم بالتحكم الصريح في تعريفات القائمة.

## أمثلة

يوضح كيفية إنشاء مستند باستخدام عينة من جميع القوائم من مستند آخر.

```csharp
public void PrintOutAllLists()
{
    Document srcDoc = new Document(MyDir + "Rendering.docx");

    Document dstDoc = new Document();
    DocumentBuilder builder = new DocumentBuilder(dstDoc);

    foreach (List srcList in srcDoc.Lists)
    {
        List dstList = dstDoc.Lists.AddCopy(srcList);
        AddListSample(builder, dstList);
    }

    dstDoc.Save(ArtifactsDir + "Lists.PrintOutAllLists.docx");
}

private static void AddListSample(DocumentBuilder builder, List list)
{
    builder.Writeln("Sample formatting of list with ListId:" + list.ListId);
    builder.ListFormat.List = list;
    for (int i = 0; i < list.ListLevels.Count; i++)
    {
        builder.ListFormat.ListLevelNumber = i;
        builder.Writeln("Level " + i);
    }

    builder.ListFormat.RemoveNumbers();
    builder.Writeln();
}
```

يوضح كيفية إعادة تشغيل الترقيم في قائمة عن طريق نسخ القائمة.

```csharp
Document doc = new Document();

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات باستخدام رموز البادئة والمسافات البادئة.
 //يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة.
 // يمكننا أن نبدأ وننهي القائمة باستخدام خاصية "ListFormat" الموجودة في منشئ المستندات.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// قم بإنشاء قائمة من قالب Microsoft Word، ثم قم بتخصيص المستوى الأول من القائمة.
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

// يمكننا إضافة نسخة من قائمة موجودة إلى مجموعة قوائم المستند
// لإنشاء قائمة مماثلة دون إجراء أي تغييرات على القائمة الأصلية.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// قم بتطبيق القائمة الثانية على الفقرات الجديدة.
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

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

* class [List](../list/)
* مساحة الاسم [Aspose.Words.Lists](../../aspose.words.lists/)
* المجسم [Aspose.Words](../../)
