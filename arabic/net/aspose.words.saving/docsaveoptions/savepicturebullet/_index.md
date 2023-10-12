---
title: DocSaveOptions.SavePictureBullet
second_title: Aspose.Words لمراجع .NET API
description: DocSaveOptions ملكية. متىخطأ شنيع  لا يتم حفظ بيانات PictureBullet في مستند الإخراج. القيمة الافتراضية هيحقيقي .
type: docs
weight: 50
url: /ar/net/aspose.words.saving/docsaveoptions/savepicturebullet/
---
## DocSaveOptions.SavePictureBullet property

متى`خطأ شنيع` ، لا يتم حفظ بيانات PictureBullet في مستند الإخراج. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool SavePictureBullet { get; set; }
```

### ملاحظات

يتم توفير هذا الخيار لـ Word 97، والذي لا يمكنه العمل بشكل صحيح مع بيانات PictureBullet. لإزالة بيانات PictureBullet، اضبط الخيار على "خطأ".

### أمثلة

يوضح كيفية حذف بيانات PictureBullet من المستند عند الحفظ.

```csharp
Document doc = new Document(MyDir + "Image bullet points.docx");
// بعض معالجات النصوص، مثل Microsoft Word 97، غير متوافقة مع بيانات PictureBullet.
// عن طريق تعيين علامة في كائن SaveOptions،
// يمكننا تحويل جميع نقاط الصورة إلى نقاط نقطية عادية أثناء الحفظ.
DocSaveOptions saveOptions = new DocSaveOptions(SaveFormat.Doc);
saveOptions.SavePictureBullet = false;

doc.Save(ArtifactsDir + "DocSaveOptions.PictureBullets.doc", saveOptions);
```

### أنظر أيضا

* class [DocSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../docsaveoptions/)
* المجسم [Aspose.Words](../../../)


