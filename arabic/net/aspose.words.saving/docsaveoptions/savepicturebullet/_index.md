---
title: DocSaveOptions.SavePictureBullet
linktitle: SavePictureBullet
articleTitle: SavePictureBullet
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية DocSaveOptions SavePictureBullet إخراج مستندك. تحكّم بسهولة في حفظ بيانات PictureBullet لتحقيق أفضل النتائج.
type: docs
weight: 60
url: /ar/net/aspose.words.saving/docsaveoptions/savepicturebullet/
---
## DocSaveOptions.SavePictureBullet property

عندما`خطأ شنيع` لا يتم حفظ بيانات PictureBullet في مستند الإخراج. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool SavePictureBullet { get; set; }
```

## ملاحظات

تم توفير هذا الخيار لبرنامج Word 97، والذي لا يمكنه العمل بشكل صحيح مع بيانات PictureBullet. لإزالة بيانات PictureBullet، اضبط الخيار على "false".

## أمثلة

يوضح كيفية حذف بيانات PictureBullet من المستند عند الحفظ.

```csharp
Document doc = new Document(MyDir + "Image bullet points.docx");
// بعض معالجات الكلمات، مثل Microsoft Word 97، غير متوافقة مع بيانات PictureBullet.
// عن طريق تعيين علم في كائن SaveOptions،
// يمكننا تحويل جميع نقاط الصورة إلى نقاط عادية أثناء الحفظ.
DocSaveOptions saveOptions = new DocSaveOptions(SaveFormat.Doc);
saveOptions.SavePictureBullet = false;

doc.Save(ArtifactsDir + "DocSaveOptions.PictureBullets.doc", saveOptions);
```

### أنظر أيضا

* class [DocSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
