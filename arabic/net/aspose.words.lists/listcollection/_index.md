---
title: ListCollection
second_title: Aspose.Words لمراجع .NET API
description: يخزن ويدير تنسيق قوائم التعداد النقطي والرقمي المستخدمة في المستند.
type: docs
weight: 3270
url: /ar/net/aspose.words.lists/listcollection/
---
## ListCollection class

يخزن ويدير تنسيق قوائم التعداد النقطي والرقمي المستخدمة في المستند.

```csharp
public class ListCollection : IEnumerable<List>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.lists/listcollection/count) { get; } | الحصول على عدد القوائم المرقمة والنقطية في المستند. |
| [Document](../../aspose.words.lists/listcollection/document) { get; } | الحصول على مستند المالك. |
| [Item](../../aspose.words.lists/listcollection/item) { get; } | يحصل على قائمة بالفهرس ._ x000d_ |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.lists/listcollection/add#add)(ListTemplate) | إنشاء قائمة جديدة بناءً على قالب محدد مسبقًا وإضافتها إلى مجموعة القوائم في المستند. |
| [Add](../../aspose.words.lists/listcollection/add#add_1)(Style) | إنشاء قائمة جديدة تشير إلى نمط قائمة وإضافتها إلى مجموعة القوائم في المستند. |
| [AddCopy](../../aspose.words.lists/listcollection/addcopy)(List) | إنشاء قائمة جديدة عن طريق نسخ القائمة المحددة وإضافتها إلى مجموعة القوائم في المستند. |
| [GetEnumerator](../../aspose.words.lists/listcollection/getenumerator)() | الحصول على كائن العداد الذي سيقوم بتعداد القوائم في المستند. |
| [GetListByListId](../../aspose.words.lists/listcollection/getlistbylistid)(int) | الحصول على قائمة بواسطة معرف القائمة . |

### ملاحظات

القائمة في مستند Microsoft Word عبارة عن مجموعة من خصائص تنسيق القائمة. _ x000d_ يتم تخزين تنسيق القوائم في[`ListCollection`](../listcollection) جمع بشكل منفصل من فقرات النص.

لا تقوم بإنشاء كائنات من هذه الفئة. هناك دائما واحد فقط[`ListCollection`](../listcollection) كائن لكل مستند ويمكن الوصول إليه عبر ملف[`Lists`](../../aspose.words/documentbase/lists) منشأه.

لإنشاء قائمة جديدة استنادًا إلى قالب قائمة محدد مسبقًا أو استنادًا إلى نمط قائمة ، استخدم [`Add`](./add) طريقة.

لإنشاء قائمة جديدة بتنسيق مماثل لقائمة موجودة ، استخدم [`AddCopy`](./addcopy) طريقة.

لجعل فقرة ذات تعداد نقطي أو رقمي ، تحتاج إلى تطبيق تنسيق القائمة_ x000d_ على فقرة من خلال تعيين[`List`](../list) الكائن على [`List`](../listformat/list) ممتلكات[`ListFormat`](../listformat).

لإزالة تنسيق القائمة من فقرة ، استخدم[`RemoveNumbers`](../listformat/removenumbers) طريقة .

إذا كنت تعرف القليل عن WordprocessingML ، فقد تعلم أنه يعرّف مفاهيم منفصلة لـ "قائمة" و "تعريف القائمة". هذا يتوافق تمامًا مع كيفية تخزين تنسيق القائمة_ x000d_ في مستند Microsoft Word بالمستوى المنخفض. تعريف القائمة يشبه "المخطط" وقائمة x000d_ مثل مثيل لتعريف القائمة.

لتبسيط نموذج البرمجة ، يخفي Aspose.Words التمييز بين تعريف list بنفس الطريقة التي يخفي بها Microsoft Word هذا في واجهة المستخدم الخاصة به. بناء كائنات منخفضة المستوى لتلبية متطلبات تنسيق ملف Microsoft Word.

لا يمكن حذف القوائم بمجرد إنشائها في الإصدار الحالي من Aspose.Words. هذا مشابه لمايكروسوفت وورد حيث لا يملك المستخدم سيطرة صريحة على تعريفات القائمة.

### أمثلة

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

يوضح كيفية إعادة تشغيل الترقيم في قائمة عن طريق نسخ قائمة.

```csharp
Document doc = new Document();

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات برموز بادئة ومسافات بادئة.
// يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة. 
// يمكننا بدء قائمة وإنهائها باستخدام خاصية "تنسيق القائمة" الخاصة بمنشئ المستندات. 
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// أنشئ قائمة من قالب Microsoft Word ، وخصص مستوى القائمة الأول.
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

// يمكننا إضافة نسخة من قائمة موجودة إلى مجموعة قائمة المستندات
// لإنشاء قائمة مماثلة دون إجراء تغييرات على الأصل.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// تطبيق القائمة الثانية على الفقرات الجديدة.
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

* class [List](../list)
* مساحة الاسم [Aspose.Words.Lists](../../aspose.words.lists)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
