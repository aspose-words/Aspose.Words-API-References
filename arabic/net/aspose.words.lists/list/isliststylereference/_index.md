---
title: List.IsListStyleReference
second_title: Aspose.Words لمراجع .NET API
description: List ملكية. إرجاع صحيح إذا كانت هذه القائمة تشير إلى نمط قائمة .
type: docs
weight: 30
url: /ar/net/aspose.words.lists/list/isliststylereference/
---
## List.IsListStyleReference property

إرجاع صحيح إذا كانت هذه القائمة تشير إلى نمط قائمة .

```csharp
public bool IsListStyleReference { get; }
```

### ملاحظات

لاحظ أن تعديل خصائص قائمة تمثل مرجعًا لنمط القائمة ليس له أي تأثير . تنسيق القائمة المحدد في نمط القائمة نفسه دائمًا ما يكون له الأسبقية.

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


