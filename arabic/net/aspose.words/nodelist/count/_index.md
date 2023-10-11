---
title: NodeList.Count
second_title: Aspose.Words لمراجع .NET API
description: NodeList ملكية. الحصول على عدد العقد في القائمة.
type: docs
weight: 10
url: /ar/net/aspose.words/nodelist/count/
---
## NodeList.Count property

الحصول على عدد العقد في القائمة.

```csharp
public int Count { get; }
```

### أمثلة

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

#if NET48 || JAVA
builder.InsertImage(Image.FromFile(ImageDir + "Logo.jpg"));
#elif NET5_0_OR_GREATER || __MOBILE__
using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
    builder.InsertImage(image);
#endif

// تحتوي وثيقتنا على ثلاث عقد تشغيل.
NodeList nodeList = doc.SelectNodes("//يجري");

Assert.AreEqual(3, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Hello world!"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// استخدم شرطة مائلة مزدوجة لتحديد جميع عقد التشغيل
// التي هي أحفاد غير مباشرة لعقدة الجدول، والتي ستكون بمثابة عمليات التشغيل داخل الخليتين اللتين أدخلناهما.
nodeList = doc.SelectNodes("//Table//يجري");

Assert.AreEqual(2, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// تحدد الخطوط المائلة الأمامية المفردة العلاقات السليلة المباشرة،
// والتي قمنا بتخطيها عندما استخدمنا الشرطة المائلة المزدوجة.
Assert.AreEqual(doc.SelectNodes(" //الجدول//تشغيل")،
    doc.SelectNodes("//جدول/صف/خلية/فقرة/تشغيل"));

// الوصول إلى الشكل الذي يحتوي على الصورة التي قمنا بإدراجها.
nodeList = doc.SelectNodes("//شكل");

Assert.AreEqual(1, nodeList.Count);

Shape shape = (Shape)nodeList[0];
Assert.True(shape.HasImage);
```

### أنظر أيضا

* class [NodeList](../)
* مساحة الاسم [Aspose.Words](../../nodelist/)
* المجسم [Aspose.Words](../../../)


