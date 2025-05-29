---
title: List.IsMultiLevel
linktitle: IsMultiLevel
articleTitle: IsMultiLevel
second_title: Aspose.Words لـ .NET
description: اكتشف ما إذا كانت قائمتك تدعم مستويات متعددة! تُظهر أداتنا صحة 9 مستويات وخطأ مستوى واحد، مما يُحسّن كفاءة إدارة بياناتك.
type: docs
weight: 40
url: /ar/net/aspose.words.lists/list/ismultilevel/
---
## List.IsMultiLevel property

إرجاع`حقيقي` عندما تحتوي القائمة على 9 مستويات؛`خطأ شنيع` عندما يكون المستوى 1.

```csharp
public bool IsMultiLevel { get; }
```

## ملاحظات

القوائم التي تقوم بإنشائها باستخدام Aspose.Words هي دائمًا قوائم متعددة المستويات وتحتوي على 9 مستويات.

يقوم Microsoft Word 2003 والإصدارات الأحدث دائمًا بإنشاء قوائم متعددة المستويات تحتوي على 9 مستويات. ولكن في بعض المستندات التي تم إنشاؤها باستخدام إصدارات سابقة من Microsoft Word، قد تواجه قوائم تحتوي على مستوى واحد فقط.

## أمثلة

يوضح كيفية إنشاء نمط القائمة واستخدامه في مستند.

```csharp
Document doc = new Document();

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات باستخدام رموز البادئة والمسافات البادئة.
 //يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة.
 // يمكننا أن نبدأ وننهي القائمة باستخدام خاصية "ListFormat" الموجودة في منشئ المستندات.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
//يمكننا أن نحتوي على كائن قائمة كامل داخل نمط.
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// تغيير مظهر جميع مستويات القائمة في قائمتنا.
foreach (ListLevel level in list1.ListLevels)
{
    level.Font.Name = "Verdana";
    level.Font.Color = Color.Blue;
    level.Font.Bold = true;
}

DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Using list style first time:");

// إنشاء قائمة أخرى من قائمة داخل نمط.
List list2 = doc.Lists.Add(listStyle);

Assert.False(list2.IsListStyleDefinition);
Assert.True(list2.IsListStyleReference);
Assert.AreEqual(listStyle, list2.Style);

//أضف بعض عناصر القائمة التي ستقوم قائمتنا بتنسيقها.
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Writeln("Using list style second time:");

// إنشاء قائمة أخرى وتطبيقها بناءً على نمط القائمة.
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

### أنظر أيضا

* class [List](../)
* مساحة الاسم [Aspose.Words.Lists](../../../aspose.words.lists/)
* المجسم [Aspose.Words](../../../)
