---
title: NodeList.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية NodeList Count لاسترداد العدد الإجمالي للعقد في قائمتك بسهولة، مما يعزز كفاءة تطوير الويب لديك.
type: docs
weight: 10
url: /ar/net/aspose.words/nodelist/count/
---
## NodeList.Count property

يحصل على عدد العقد في القائمة.

```csharp
public int Count { get; }
```

## أمثلة

يوضح كيفية استخدام XPaths للتنقل في NodeList.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل بعض العقد باستخدام DocumentBuilder.
builder.Writeln("Hello world!");

builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();

builder.InsertImage(ImageDir + "Logo.jpg");

// تحتوي مستندنا على ثلاث عقد تشغيل.
NodeList nodeList = doc.SelectNodes("//يجري");

Assert.AreEqual(3, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Hello world!"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// استخدم شرطة مائلة مزدوجة للأمام لتحديد جميع عقد التشغيل
// التي هي أحفاد غير مباشرين لعقدة الجدول، والتي ستكون عبارة عن عمليات تشغيل داخل الخليتين اللتين أدخلناهما.
nodeList = doc.SelectNodes("//Table//يجري");

Assert.AreEqual(2, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// تشير الخطوط المائلة للأمام الفردية إلى علاقات النسل المباشرة،
// والتي تخطيناها عندما استخدمنا الشرطات المزدوجة.
Assert.AreEqual(doc.SelectNodes(" //الجدول//تشغيل"),
    doc.SelectNodes("//الجدول/الصف/الخلية/الفقرة/التشغيل"));

//الوصول إلى الشكل الذي يحتوي على الصورة التي أدخلناها.
nodeList = doc.SelectNodes("//شكل");

Assert.AreEqual(1, nodeList.Count);

Shape shape = (Shape)nodeList[0];
Assert.True(shape.HasImage);
```

### أنظر أيضا

* class [NodeList](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
