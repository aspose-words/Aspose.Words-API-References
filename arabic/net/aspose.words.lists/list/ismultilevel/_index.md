---
title: List.IsMultiLevel
second_title: Aspose.Words لمراجع .NET API
description: List ملكية. إرجاع صحيح عندما تحتوي القائمة على 9 مستويات  خطأ عند المستوى الأول .
type: docs
weight: 40
url: /ar/net/aspose.words.lists/list/ismultilevel/
---
## List.IsMultiLevel property

إرجاع صحيح عندما تحتوي القائمة على 9 مستويات ؛ خطأ عند المستوى الأول .

```csharp
public bool IsMultiLevel { get; }
```

### ملاحظات

القوائم التي تقوم بإنشائها باستخدام Aspose.Words هي دائمًا قوائم متعددة المستويات وتحتوي على 9 مستويات.

يقوم Microsoft Word 2003 والإصدارات الأحدث دائمًا بإنشاء قوائم متعددة المستويات مع 9 مستويات . لكن في بعض المستندات ، التي تم إنشاؤها باستخدام إصدارات سابقة من Microsoft Word ، قد تواجه قوائم تحتوي على مستوى واحد فقط.

### أمثلة

يوضح كيفية إنشاء نمط قائمة واستخدامه في مستند.

```csharp
Document doc = new Document();

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات برموز بادئة ومسافات بادئة.
// يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة. 
// يمكننا بدء قائمة وإنهائها باستخدام خاصية "تنسيق القائمة" الخاصة بمنشئ المستندات. 
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// يمكننا احتواء كائن قائمة كامل داخل نمط.
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

// إنشاء قائمة أخرى من قائمة داخل النمط.
List list2 = doc.Lists.Add(listStyle);

Assert.False(list2.IsListStyleDefinition);
Assert.True(list2.IsListStyleReference);
Assert.AreEqual(listStyle, list2.Style);

// أضف بعض عناصر القائمة التي ستقوم قائمتنا بتنسيقها.
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Writeln("Using list style second time:");

// إنشاء وتطبيق قائمة أخرى بناءً على نمط القائمة.
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

### أنظر أيضا

* class [List](../)
* مساحة الاسم [Aspose.Words.Lists](../../list/)
* المجسم [Aspose.Words](../../../)


