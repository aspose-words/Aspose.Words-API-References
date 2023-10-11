---
title: Fill.SetImage
second_title: Aspose.Words لمراجع .NET API
description: Fill طريقة. تغيير نوع التعبئة إلى صورة واحدة.
type: docs
weight: 250
url: /ar/net/aspose.words.drawing/fill/setimage/
---
## SetImage(string) {#setimage_2}

تغيير نوع التعبئة إلى صورة واحدة.

```csharp
public void SetImage(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | المسار إلى ملف الصورة. |

### أمثلة

يوضح كيفية تعيين نوع تعبئة الشكل كصورة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// هناك عدة طرق لإعداد الصورة.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 1 - استخدام اسم ملف النظام المحلي:
shape.Fill.SetImage(ImageDir + "Logo.jpg");
doc.Save(ArtifactsDir + "Shape.FillImage.FileName.docx");

// 2 - تحميل ملف إلى مصفوفة بايت:
shape.Fill.SetImage(File.ReadAllBytes(ImageDir + "Logo.jpg"));
doc.Save(ArtifactsDir + "Shape.FillImage.ByteArray.docx");

// 3 - من الدفق:
using (FileStream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
    shape.Fill.SetImage(stream);
doc.Save(ArtifactsDir + "Shape.FillImage.Stream.docx");
```

### أنظر أيضا

* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../fill/)
* المجسم [Aspose.Words](../../../)

---

## SetImage(Stream) {#setimage_1}

تغيير نوع التعبئة إلى صورة واحدة.

```csharp
public void SetImage(Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | الدفق الذي يحتوي على بايت الصورة. |

### أنظر أيضا

* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../fill/)
* المجسم [Aspose.Words](../../../)

---

## SetImage(byte[]) {#setimage}

تغيير نوع التعبئة إلى صورة واحدة.

```csharp
public void SetImage(byte[] imageBytes)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| imageBytes | Byte[] | مجموعة بايت الصورة. |

### أنظر أيضا

* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../fill/)
* المجسم [Aspose.Words](../../../)


