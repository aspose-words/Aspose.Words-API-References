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

القائمة المنشأة حديثًا.

### ملاحظات

يمكن أن تكون قائمة المصادر من أي مستند. إذا كانت قائمة المصادر تنتمي إلى مستند مختلف ، فسيتم إنشاء نسخة من القائمة وإضافتها إلى المستند الحالي .

إذا كانت قائمة المصادر مرجعًا لنمط قائمة أو تعريفًا له ، فإن القائمة المنشأة حديثًا لا تتعلق بنمط القائمة الأصلي.

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

### أنظر أيضا

* class [List](../../list/)
* class [ListCollection](../)
* مساحة الاسم [Aspose.Words.Lists](../../listcollection/)
* المجسم [Aspose.Words](../../../)


