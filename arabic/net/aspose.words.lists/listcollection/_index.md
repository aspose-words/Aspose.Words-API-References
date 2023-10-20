---
title: ListCollection Class
linktitle: ListCollection
articleTitle: ListCollection
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Lists.ListCollection فصل. يقوم بتخزين وإدارة تنسيق القوائم ذات التعداد النقطي والرقمي المستخدمة في المستند في C#.
type: docs
weight: 3470
url: /ar/net/aspose.words.lists/listcollection/
---
## ListCollection class

يقوم بتخزين وإدارة تنسيق القوائم ذات التعداد النقطي والرقمي المستخدمة في المستند.

لمعرفة المزيد، قم بزيارة[العمل مع القوائم](https://docs.aspose.com/words/net/working-with-lists/) مقالة توثيقية.

```csharp
public class ListCollection : IEnumerable<List>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.lists/listcollection/count/) { get; } | الحصول على عدد القوائم المرقمة والتعداد النقطي في المستند. |
| [Document](../../aspose.words.lists/listcollection/document/) { get; } | الحصول على مستند المالك. |
| [Item](../../aspose.words.lists/listcollection/item/) { get; } | الحصول على قائمة حسب الفهرس. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.lists/listcollection/add/#add)(*[ListTemplate](../listtemplate/)*) | إنشاء قائمة جديدة بناءً على قالب محدد مسبقًا وإضافتها إلى مجموعة القوائم في المستند. |
| [Add](../../aspose.words.lists/listcollection/add/#add_1)(*[Style](../../aspose.words/style/)*) | إنشاء قائمة جديدة تشير إلى نمط قائمة وإضافته إلى مجموعة القوائم في المستند. |
| [AddCopy](../../aspose.words.lists/listcollection/addcopy/)(*[List](../list/)*) | إنشاء قائمة جديدة عن طريق نسخ القائمة المحددة وإضافتها إلى مجموعة القوائم في المستند. |
| [GetEnumerator](../../aspose.words.lists/listcollection/getenumerator/)() | الحصول على كائن العداد الذي سيقوم بتعداد القوائم في المستند. |
| [GetListByListId](../../aspose.words.lists/listcollection/getlistbylistid/)(*int*) | الحصول على قائمة حسب معرف القائمة. |

## ملاحظات

القائمة الموجودة في مستند Microsoft Word هي مجموعة من خصائص تنسيق القائمة. يتم تخزين تنسيق القوائم في`ListCollection` جمع بشكل منفصل من فقرات النص.

لا تقم بإنشاء كائنات من هذه الفئة. هناك دائما واحد فقط`ListCollection` كائن لكل مستند ويمكن الوصول إليه عبر[`Lists`](../../aspose.words/documentbase/lists/) ملكية.

لإنشاء قائمة جديدة بناءً على قالب قائمة محدد مسبقًا أو بناءً على نمط القائمة، استخدم[`Add`](./add/) طريقة.

لإنشاء قائمة جديدة بتنسيق مماثل لقائمة موجودة، استخدم[`AddCopy`](./addcopy/) طريقة.

لجعل فقرة ذات تعداد نقطي أو رقمي، تحتاج إلى تطبيق تنسيق القائمة على فقرة عن طريق تعيين[`List`](../list/)الاعتراض على the [`List`](../listformat/list/) ممتلكات[`ListFormat`](../listformat/).

لإزالة تنسيق القائمة من فقرة، استخدم الأمر[`RemoveNumbers`](../listformat/removenumbers/) طريقة .

إذا كنت تعرف القليل عن WordprocessingML، فربما تعلم أنه يحدد مفاهيم منفصلة لـ "القائمة" و"تعريف القائمة". يتوافق هذا تمامًا مع كيفية تخزين تنسيق القائمة في مستند Microsoft Word على المستوى المنخفض. تعريف القائمة يشبه "المخطط" وقائمة تشبه مثيل تعريف القائمة.

لتبسيط نموذج البرمجة، يخفي Aspose.Words الفرق بين تعريف القائمة وتعريف list بنفس الطريقة التي يخفي بها Microsoft Word هذا في واجهة المستخدم الخاصة به. وهذا يسمح لك بالتركيز بشكل أكبر على الشكل الذي تريد أن يبدو عليه مستندك، بدلاً من إنشاء كائنات منخفضة المستوى لتلبية متطلبات تنسيق ملف Microsoft Word.

ليس من الممكن حذف القوائم بمجرد إنشائها في الإصدار الحالي من Aspose.Words. وهذا يشبه Microsoft Word حيث لا يملك المستخدم تحكمًا صريحًا في تعريفات القائمة.

## أمثلة

يوضح كيفية إنشاء مستند باستخدام عينة من كافة القوائم من مستند آخر.

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

* class [List](../list/)
* مساحة الاسم [Aspose.Words.Lists](../../aspose.words.lists/)
* المجسم [Aspose.Words](../../)
