---
title: ListLevel.CreatePictureBullet
linktitle: CreatePictureBullet
articleTitle: CreatePictureBullet
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة ListLevel CreatePictureBullet لتحسين قوائمك بسهولة باستخدام نقاط الصور المخصصة، مما يضيف جاذبية بصرية ووضوحًا.
type: docs
weight: 150
url: /ar/net/aspose.words.lists/listlevel/createpicturebullet/
---
## ListLevel.CreatePictureBullet method

ينشئ شكل نقطي للصورة لمستوى القائمة الحالي.

```csharp
public void CreatePictureBullet()
```

## ملاحظات

يرجى الملاحظة،[`NumberStyle`](../numberstyle/) سيتم ضبطه علىBullet و [`NumberFormat`](../numberformat/) إلى "\xF0B7" لعرض صورة نقطية بشكل صحيح. سيتم تعيين صورة الصليب الأحمر كصورة نقطية عند إنشائها. لتغييرها، يرجى استخدام[`ImageData`](../imagedata/).

## أمثلة

يوضح كيفية تعيين أيقونة صورة مخصصة لعناوين عناصر القائمة.

```csharp
Document doc = new Document();

List list = doc.Lists.Add(ListTemplate.BulletCircle);

// قم بإنشاء صورة نقطية لمستوى القائمة الحالي، وقم بتعيين صورة من نظام ملفات محلي
// كالأيقونة التي ستظهر بها النقاط الخاصة بمستوى القائمة هذا.
list.ListLevels[0].CreatePictureBullet();
list.ListLevels[0].ImageData.SetImage(ImageDir + "Logo icon.ico");

Assert.IsTrue(list.ListLevels[0].ImageData.HasImage);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("Hello world!");
builder.Write("Hello again!");

doc.Save(ArtifactsDir + "Lists.CreatePictureBullet.docx");

list.ListLevels[0].DeletePictureBullet();

Assert.IsNull(list.ListLevels[0].ImageData);
```

### أنظر أيضا

* class [ListLevel](../)
* مساحة الاسم [Aspose.Words.Lists](../../../aspose.words.lists/)
* المجسم [Aspose.Words](../../../)
