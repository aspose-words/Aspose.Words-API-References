---
title: Converter.ConvertToImages
linktitle: ConvertToImages
articleTitle: ConvertToImages
second_title: Aspose.Words لـ .NET
description: حوّل مستنداتك بسهولة مع ConvertToImages. حوّل الصفحات إلى ملفات صور عالية الجودة بسرعة وسهولة لتحسين مشاركتها وتخزينها.
type: docs
weight: 30
url: /ar/net/aspose.words.lowcode/converter/converttoimages/
---
## ConvertToImages(*string, [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages_5}

يحول صفحات ملف الإدخال المحدد إلى صور بالتنسيق المحدد ويعيد مجموعة من التدفقات التي تحتوي على الصور.

```csharp
public static Stream[] ConvertToImages(string inputFile, SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFile | String | اسم ملف الإدخال. |
| saveFormat | SaveFormat | حفظ الصيغة. يُسمح فقط بصيغ حفظ الصور. |

### قيمة الإرجاع

يُرجع مصفوفة من تدفقات الصور. يجب على المستخدم التخلص من هذه التدفقات.

## أمثلة

يوضح كيفية تحويل المستند إلى تدفق الصور.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## ConvertToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_6}

يحول صفحات ملف الإدخال المحدد إلى صور باستخدام خيارات الحفظ المحددة ويعيد مجموعة من التدفقات التي تحتوي على الصور.

```csharp
public static Stream[] ConvertToImages(string inputFile, ImageSaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFile | String | اسم ملف الإدخال. |
| saveOptions | ImageSaveOptions | خيارات حفظ الصورة. |

### قيمة الإرجاع

يُرجع مصفوفة من تدفقات الصور. يجب على المستخدم التخلص من هذه التدفقات.

## أمثلة

يوضح كيفية تحويل المستند إلى تدفق الصور.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages_3}

يحول صفحات مجرى الإدخال المحدد إلى صور بالتنسيق المحدد ويعيد مجموعة من المجاري التي تحتوي على الصور.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | مجرى الإدخال. |
| saveFormat | SaveFormat | حفظ الصيغة. يُسمح فقط بصيغ حفظ الصور. |

### قيمة الإرجاع

يُرجع مصفوفة من تدفقات الصور. يجب على المستخدم التخلص من هذه التدفقات.

## أمثلة

يوضح كيفية تحويل المستند إلى صور من التدفق.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_4}

يحول صفحات مجرى الإدخال المحدد إلى صور باستخدام خيارات الحفظ المحددة ويعيد مجموعة من المجاري التي تحتوي على الصور.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, ImageSaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | مجرى الإدخال. |
| saveOptions | ImageSaveOptions | خيارات حفظ الصورة. |

### قيمة الإرجاع

يُرجع مصفوفة من تدفقات الصور. يجب على المستخدم التخلص من هذه التدفقات.

## أمثلة

يوضح كيفية تحويل المستند إلى صور من التدفق.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/), [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_2}

يحول صفحات مجرى الإدخال المحدد إلى صور باستخدام خيارات التحميل والحفظ المقدمة، ويعيد مجموعة من المجاري التي تحتوي على الصور.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, LoadOptions loadOptions, 
    ImageSaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | مجرى الإدخال. |
| loadOptions | LoadOptions | خيارات تحميل مستند الإدخال. |
| saveOptions | ImageSaveOptions | خيارات حفظ الصورة. |

### قيمة الإرجاع

يُرجع مصفوفة من تدفقات الصور. يجب على المستخدم التخلص من هذه التدفقات.

## أمثلة

يوضح كيفية تحويل المستند إلى صور من التدفق.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### أنظر أيضا

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## ConvertToImages(*[Document](../../../aspose.words/document/), [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages}

يحول صفحات المستند المحدد إلى صور بالتنسيق المحدد ويعيد مجموعة من التدفقات التي تحتوي على الصور.

```csharp
public static Stream[] ConvertToImages(Document doc, SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| doc | Document | وثيقة الإدخال. |
| saveFormat | SaveFormat | حفظ الصيغة. يُسمح فقط بصيغ حفظ الصور. |

### قيمة الإرجاع

يُرجع مصفوفة من تدفقات الصور. يجب على المستخدم التخلص من هذه التدفقات.

## أمثلة

يوضح كيفية تحويل المستند إلى تدفق الصور.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### أنظر أيضا

* class [Document](../../../aspose.words/document/)
* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## ConvertToImages(*[Document](../../../aspose.words/document/), [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_1}

يحول صفحات المستند المحدد إلى صور باستخدام خيارات الحفظ المحددة ويعيد مجموعة من التدفقات التي تحتوي على الصور.

```csharp
public static Stream[] ConvertToImages(Document doc, ImageSaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| doc | Document | وثيقة الإدخال. |
| saveOptions | ImageSaveOptions | خيارات حفظ الصورة. |

### قيمة الإرجاع

يُرجع مصفوفة من تدفقات الصور. يجب على المستخدم التخلص من هذه التدفقات.

## أمثلة

يوضح كيفية تحويل المستند إلى تدفق الصور.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### أنظر أيضا

* class [Document](../../../aspose.words/document/)
* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
