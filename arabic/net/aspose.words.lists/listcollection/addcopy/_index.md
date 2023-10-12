---
title: ListCollection.AddCopy
second_title: Aspose.Words لمراجع .NET API
description: ListCollection طريقة. إنشاء قائمة جديدة عن طريق نسخ القائمة المحددة وإضافتها إلى مجموعة القوائم في المستند.
type: docs
weight: 50
url: /ar/net/aspose.words.lists/listcollection/addcopy/
---
## ListCollection.AddCopy method

إنشاء قائمة جديدة عن طريق نسخ القائمة المحددة وإضافتها إلى مجموعة القوائم في المستند.

```csharp
public List AddCopy(List srcList)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcList | List | قائمة المصادر المراد النسخ منها. |

### قيمة الإرجاع

القائمة التي تم إنشاؤها حديثا.

### ملاحظات

يمكن أن تكون قائمة المصدر من أي مستند. إذا كانت القائمة المصدر تنتمي إلى مستند مختلف، فسيتم إنشاء نسخة من القائمة وإضافتها إلى المستند الحالي.

إذا كانت القائمة المصدر مرجعًا أو تعريفًا لنمط القائمة، فإن القائمة التي تم إنشاؤها حديثًا لا ترتبط بنمط القائمة الأصلي.

### أمثلة

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

### أنظر أيضا

* class [List](../../list/)
* class [ListCollection](../)
* مساحة الاسم [Aspose.Words.Lists](../../listcollection/)
* المجسم [Aspose.Words](../../../)


