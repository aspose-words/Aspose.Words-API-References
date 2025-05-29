---
title: ListLevel.DeletePictureBullet
linktitle: DeletePictureBullet
articleTitle: DeletePictureBullet
second_title: Aspose.Words لـ .NET
description: احذف نقاط الصور بسهولة من مستوى قائمتك الحالي باستخدام طريقة ListLevel DeletePictureBullet. بسّط تنسيق مستندك اليوم!
type: docs
weight: 160
url: /ar/net/aspose.words.lists/listlevel/deletepicturebullet/
---
## ListLevel.DeletePictureBullet method

يحذف صورة النقطة لمستوى القائمة الحالي.

```csharp
public void DeletePictureBullet()
```

## ملاحظات

سيتم عرض الرصاصة الافتراضية بعد الحذف.

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
