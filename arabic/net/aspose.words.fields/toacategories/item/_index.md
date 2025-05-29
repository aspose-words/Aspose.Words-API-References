---
title: ToaCategories.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: أدر عناصر ToaCategories بسهولة. حدّد عناوين الفئات واسترجاعها بسهولة حسب الرقم، مما يُسهّل التنظيم ويزيد من الكفاءة.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/toacategories/item/
---
## ToaCategories indexer

يحصل على عنوان الفئة أو يعينه حسب رقم الفئة.

```csharp
public string this[int number] { get; set; }
```

## أمثلة

يوضح كيفية تحديد مجموعة من الفئات لحقول TOA.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يمكن لحقول TOA تصفية إدخالاتها حسب الفئات المحددة في هذه المجموعة.
ToaCategories toaCategories = new ToaCategories();
doc.FieldOptions.ToaCategories = toaCategories;

//تأتي هذه المجموعة من الفئات بقيم افتراضية، والتي يمكننا استبدالها بقيم مخصصة.
Assert.AreEqual("Cases", toaCategories[1]);
Assert.AreEqual("Statutes", toaCategories[2]);

toaCategories[1] = "My Category 1";
toaCategories[2] = "My Category 2";

//يمكننا دائمًا الوصول إلى القيم الافتراضية عبر هذه المجموعة.
Assert.AreEqual("Cases", ToaCategories.DefaultCategories[1]);
Assert.AreEqual("Statutes", ToaCategories.DefaultCategories[2]);

// إدراج حقلين TOA. تقوم حقول TOA بإنشاء إدخال لكل حقل TA في المستند.
// استخدم المفتاح "\c" لتحديد فهرس الفئة من مجموعتنا.
// باستخدام هذا التبديل، سوف يلتقط حقل TOA فقط الإدخالات من حقول TA التي
// يوجد أيضًا مفتاح "\c" مع فهرس فئة مطابق. سيعرض كل حقل TOA أيضًا
// اسم الفئة التي يشير إليها مفتاح "\c".
builder.InsertField("TOA \\c 1 \\h", null);
builder.InsertField("TOA \\c 2 \\h", null);
builder.InsertBreak(BreakType.PageBreak);

// أدخل إدخالات TOA في فئتين. سيستقبل حقل TOA الأول إدخالاً واحدًا،
// من حقل TA الثاني الذي يشير مفتاحه "\c" أيضًا إلى الفئة الأولى.
// سيحتوي حقل TOA الثاني على إدخالين من حقلي TA الآخرين.
builder.InsertField("TA \\c 2 \\l \"entry 1\"");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertField("TA \\c 1 \\l \"entry 2\"");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertField("TA \\c 2 \\l \"entry 3\"");

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.TOA.Categories.docx");
```

### أنظر أيضا

* class [ToaCategories](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
