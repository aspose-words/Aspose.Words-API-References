---
title: FileFormatUtil.ContentTypeToLoadFormat
second_title: Aspose.Words لمراجع .NET API
description: FileFormatUtil طريقة. تحويل نوع محتوى IANA إلى قيمة تعدادية لتنسيق التحميل.
type: docs
weight: 10
url: /ar/net/aspose.words/fileformatutil/contenttypetoloadformat/
---
## FileFormatUtil.ContentTypeToLoadFormat method

تحويل نوع محتوى IANA إلى قيمة تعدادية لتنسيق التحميل.

```csharp
public static LoadFormat ContentTypeToLoadFormat(string contentType)
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentException | يرمي عندما لا يمكن تحويل. |

### أمثلة

يوضح كيفية العثور على تنسيق Aspose التحميل/الحفظ المطابق من كل سلسلة من أنواع الوسائط.

```csharp
 // تقبل أساليب ContentTypeToSaveFormat/ContentTypeToLoadFormat فقط أسماء أنواع وسائط IANA الرسمية، والمعروفة أيضًا بأنواع MIME.
// جميع أنواع الوسائط الصالحة مدرجة هنا: https://www.iana.org/signments/media-types/media-types.xhtml.

// لن تنجح محاولة ربط SaveFormat بسلسلة من نوع الوسائط الجزئية.
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToSaveFormat("jpeg"));

// إذا لم يكن لدى Aspose.Words تنسيق حفظ/تحميل مطابق لنوع المحتوى، فسيتم طرح استثناء أيضًا.
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToSaveFormat("application/zip"));

// يمكن حفظ الملفات من الأنواع المذكورة أدناه، ولكن لا يمكن تحميلها باستخدام Aspose.Words.
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToLoadFormat("image/jpeg"));

Assert.AreEqual(SaveFormat.Jpeg, FileFormatUtil.ContentTypeToSaveFormat("image/jpeg"));
Assert.AreEqual(SaveFormat.Png, FileFormatUtil.ContentTypeToSaveFormat("image/png"));
Assert.AreEqual(SaveFormat.Tiff, FileFormatUtil.ContentTypeToSaveFormat("image/tiff"));
Assert.AreEqual(SaveFormat.Gif, FileFormatUtil.ContentTypeToSaveFormat("image/gif"));
Assert.AreEqual(SaveFormat.Emf, FileFormatUtil.ContentTypeToSaveFormat("image/x-emf"));
Assert.AreEqual(SaveFormat.Xps, FileFormatUtil.ContentTypeToSaveFormat("application/vnd.ms-xpsdocument"));
Assert.AreEqual(SaveFormat.Pdf, FileFormatUtil.ContentTypeToSaveFormat("application/pdf"));
Assert.AreEqual(SaveFormat.Svg, FileFormatUtil.ContentTypeToSaveFormat("image/svg+xml"));
Assert.AreEqual(SaveFormat.Epub, FileFormatUtil.ContentTypeToSaveFormat("application/epub+zip"));

// بالنسبة لأنواع الملفات التي يمكن حفظها وتحميلها، يمكننا مطابقة نوع الوسائط مع كل من تنسيق التحميل وتنسيق الحفظ.
Assert.AreEqual(LoadFormat.Doc, FileFormatUtil.ContentTypeToLoadFormat("application/msword"));
Assert.AreEqual(SaveFormat.Doc, FileFormatUtil.ContentTypeToSaveFormat("application/msword"));

Assert.AreEqual(LoadFormat.Docx,
    FileFormatUtil.ContentTypeToLoadFormat(
        "application/vnd.openxmlformats-officedocument.wordprocessingml.document"));
Assert.AreEqual(SaveFormat.Docx,
    FileFormatUtil.ContentTypeToSaveFormat(
        "application/vnd.openxmlformats-officedocument.wordprocessingml.document"));

Assert.AreEqual(LoadFormat.Text, FileFormatUtil.ContentTypeToLoadFormat("text/plain"));
Assert.AreEqual(SaveFormat.Text, FileFormatUtil.ContentTypeToSaveFormat("text/plain"));

Assert.AreEqual(LoadFormat.Rtf, FileFormatUtil.ContentTypeToLoadFormat("application/rtf"));
Assert.AreEqual(SaveFormat.Rtf, FileFormatUtil.ContentTypeToSaveFormat("application/rtf"));

Assert.AreEqual(LoadFormat.Html, FileFormatUtil.ContentTypeToLoadFormat("text/html"));
Assert.AreEqual(SaveFormat.Html, FileFormatUtil.ContentTypeToSaveFormat("text/html"));

Assert.AreEqual(LoadFormat.Mhtml, FileFormatUtil.ContentTypeToLoadFormat("multipart/related"));
Assert.AreEqual(SaveFormat.Mhtml, FileFormatUtil.ContentTypeToSaveFormat("multipart/related"));
```

### أنظر أيضا

* enum [LoadFormat](../../loadformat/)
* class [FileFormatUtil](../)
* مساحة الاسم [Aspose.Words](../../fileformatutil/)
* المجسم [Aspose.Words](../../../)


