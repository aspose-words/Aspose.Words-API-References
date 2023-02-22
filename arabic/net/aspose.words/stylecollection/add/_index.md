---
title: StyleCollection.Add
second_title: Aspose.Words لمراجع .NET API
description: StyleCollection طريقة. ينشئ نمطًا جديدًا معرّفًا من قبل المستخدم ويضيفه إلى المجموعة.
type: docs
weight: 60
url: /ar/net/aspose.words/stylecollection/add/
---
## StyleCollection.Add method

ينشئ نمطًا جديدًا معرّفًا من قبل المستخدم ويضيفه إلى المجموعة.

```csharp
public Style Add(StyleType type, string name)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| type | StyleType | أ[`StyleType`](../../styletype/) القيمة التي تحدد نوع النمط المراد إنشاؤه. |
| name | String | اسم حساس لحالة الأحرف للنمط المراد إنشاؤه. |

### ملاحظات

يمكنك إنشاء حرف أو فقرة أو نمط قائمة.

عند إنشاء نمط قائمة ، يتم إنشاء النمط بتنسيق افتراضي لقائمة مرقمة (1 \ a \ i).

يطرح استثناء في حالة وجود نمط بهذا الاسم بالفعل.

### أمثلة

يوضح كيفية إضافة نمط إلى مجموعة أنماط المستند.

```csharp
Document doc = new Document();
StyleCollection styles = doc.Styles;

// تعيين المعلمات الافتراضية للأنماط الجديدة التي قد نضيفها لاحقًا إلى هذه المجموعة.
styles.DefaultFont.Name = "Courier New";

// إذا أضفنا نمطًا من "StyleType.Paragraph" ، فستطبق المجموعة قيم
// الخاصية "DefaultParagraphFormat" الخاصة بها إلى خاصية "تنسيق ParagraphFormat" الخاصة بالنمط.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;

// أضف نمطًا ، ثم تحقق من أنه يحتوي على الإعدادات الافتراضية.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

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

* class [Style](../../style/)
* enum [StyleType](../../styletype/)
* class [StyleCollection](../)
* مساحة الاسم [Aspose.Words](../../stylecollection/)
* المجسم [Aspose.Words](../../../)


