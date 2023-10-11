---
title: ListLevel.CreatePictureBullet
second_title: Aspose.Words لمراجع .NET API
description: ListLevel طريقة. إنشاء شكل نقطي للصورة لمستوى القائمة الحالي.
type: docs
weight: 150
url: /ar/net/aspose.words.lists/listlevel/createpicturebullet/
---
## ListLevel.CreatePictureBullet method

إنشاء شكل نقطي للصورة لمستوى القائمة الحالي.

```csharp
public void CreatePictureBullet()
```

### ملاحظات

يرجى الملاحظة،[`NumberStyle`](../numberstyle/) سيتم تعيين لBullet و [`NumberFormat`](../numberformat/) إلى "\xF0B7" لعرض الصورة بشكل صحيح. سيتم تعيين صورة الصليب الأحمر كصورة نقطية عند الإنشاء. لتغييرها، يرجى استخدام[`ImageData`](../imagedata/).

### أمثلة

يوضح كيفية تعيين رمز صورة مخصص لتسميات عناصر القائمة.

```csharp
Document doc = new Document();

List list = doc.Lists.Add(ListTemplate.BulletCircle);

// قم بإنشاء رمز نقطي لمستوى القائمة الحالي، وقم بتعيين صورة من نظام الملفات المحلي
// كأيقونة ستعرضها التعداد النقطي لمستوى القائمة هذا.
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
* مساحة الاسم [Aspose.Words.Lists](../../listlevel/)
* المجسم [Aspose.Words](../../../)


