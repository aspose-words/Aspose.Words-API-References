---
title: StyleCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة StyleCollection Add لإنشاء أنماط مخصصة محددة من قبل المستخدم وإضافتها إلى مجموعتك بسهولة، مما يعزز مرونة التصميم لديك.
type: docs
weight: 60
url: /ar/net/aspose.words/stylecollection/add/
---
## StyleCollection.Add method

ينشئ نمطًا جديدًا محددًا من قبل المستخدم ويضيفه إلى المجموعة.

```csharp
public Style Add(StyleType type, string name)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| type | StyleType | أ[`StyleType`](../../styletype/) القيمة التي تحدد نوع النمط الذي سيتم إنشاؤه. |
| name | String | اسم النمط الذي سيتم إنشاؤه حساس لحالة الأحرف. |

## ملاحظات

يمكنك إنشاء نمط حرف أو فقرة أو قائمة.

عند إنشاء نمط قائمة، يتم إنشاء النمط باستخدام تنسيق القائمة المرقمة الافتراضي (1 \ a \ i).

يُلقي استثناءً إذا كان النمط بهذا الاسم موجودًا بالفعل.

## أمثلة

يوضح كيفية إضافة نمط إلى مجموعة أنماط المستند.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// تعيين المعلمات الافتراضية للأنماط الجديدة التي قد نضيفها لاحقًا إلى هذه المجموعة.
styles.DefaultFont.Name = "Courier New";
// إذا أضفنا نمط "StyleType.Paragraph"، ستطبق المجموعة قيم
// خاصية "DefaultParagraphFormat" الخاصة بها إلى خاصية "ParagraphFormat" الخاصة بالنمط.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
//أضف نمطًا، ثم تأكد من أنه يحتوي على الإعدادات الافتراضية.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

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

* class [Style](../../style/)
* enum [StyleType](../../styletype/)
* class [StyleCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
