---
title: Replacer.ReplaceToImages
linktitle: ReplaceToImages
articleTitle: ReplaceToImages
second_title: Aspose.Words لـ .NET
description: قم بتحويل ملفات الإدخال الخاصة بك بسهولة عن طريق استبدال أنماط الأحرف بسلاسل مخصصة وإنشاء صور مذهلة باستخدام طريقة ReplaceToImages الخاصة بنا.
type: docs
weight: 30
url: /ar/net/aspose.words.lowcode/replacer/replacetoimages/
---
## ReplaceToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_2}

يستبدل جميع حالات نمط سلسلة أحرف محددة بسلسلة بديلة في ملف الإدخال. يعرض الإخراج على شكل صور.

```csharp
public static Stream[] ReplaceToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| saveOptions | ImageSaveOptions | خيارات الحفظ. |
| pattern | String | سلسلة ليتم استبدالها. |
| replacement | String | سلسلة لاستبدال كافة حالات النمط. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) كائن لتحديد خيارات إضافية. |

## أمثلة

يوضح كيفية استبدال السلسلة في المستند وحفظ النتيجة في الصور.

```csharp
// هناك عدة طرق لاستبدال السلسلة في المستند:
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

Stream[] images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);

FindReplaceOptions options = new FindReplaceOptions();
options.FindWholeWordsOnly = false;
images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, options);
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## ReplaceToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages}

يستبدل جميع حالات نمط سلسلة أحرف محددة بسلسلة بديلة في ملف الإدخال. يعرض الإخراج على شكل صور.

```csharp
public static Stream[] ReplaceToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | تدفق ملف الإدخال. |
| saveOptions | ImageSaveOptions | خيارات الحفظ. |
| pattern | String | سلسلة ليتم استبدالها. |
| replacement | String | سلسلة لاستبدال كافة حالات النمط. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) كائن لتحديد خيارات إضافية. |

## أمثلة

يوضح كيفية استبدال السلسلة في المستند باستخدام المستندات من الدفق وحفظ النتيجة في الصور.

```csharp
// هناك عدة طرق لاستبدال السلسلة في المستند باستخدام المستندات من الدفق:
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

using (FileStream streamIn = new FileStream(MyDir + "Footer.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);

    FindReplaceOptions options = new FindReplaceOptions();
    options.FindWholeWordsOnly = false;
    images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, options);
}
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## ReplaceToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_3}

يستبدل جميع حالات نمط تعبير منتظم محدد بسلسلة استبدال في ملف الإدخال. يعرض الإخراج على شكل صور.

```csharp
public static Stream[] ReplaceToImages(string inputFileName, ImageSaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| saveOptions | ImageSaveOptions | خيارات الحفظ. |
| pattern | Regex | نمط تعبير منتظم يستخدم للعثور على المطابقات. |
| replacement | String | سلسلة لاستبدال كافة حالات النمط. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) كائن لتحديد خيارات إضافية. |

## أمثلة

يوضح كيفية استبدال السلسلة بـ regex في المستند وحفظ النتيجة في الصور.

```csharp
// هناك عدة طرق لاستبدال السلسلة بـ regex في المستند:
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

Stream[] images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);
images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## ReplaceToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_1}

يستبدل جميع حالات نمط تعبير منتظم محدد بسلسلة استبدال في ملف الإدخال. يعرض الإخراج على شكل صور.

```csharp
public static Stream[] ReplaceToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | تدفق ملف الإدخال. |
| saveOptions | ImageSaveOptions | خيارات الحفظ. |
| pattern | Regex | نمط تعبير منتظم يستخدم للعثور على المطابقات. |
| replacement | String | سلسلة لاستبدال كافة حالات النمط. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) كائن لتحديد خيارات إضافية. |

## أمثلة

يوضح كيفية استبدال السلسلة بتعبير عادي في المستند باستخدام المستندات من التدفق وحفظ النتيجة في الصور.

```csharp
// هناك عدة طرق لاستبدال السلسلة بتعبير عادي في المستند باستخدام المستندات من التدفق:
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

using (FileStream streamIn = new FileStream(MyDir + "Replace regex.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);
    images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
}
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
