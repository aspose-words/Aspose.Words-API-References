---
title: GetEffectiveValue
second_title: Aspose.Words لمراجع .NET API
description: يبين تمثيل السلسلة لملفListLevelaspose.words.lists/listlevel كائن index المحدد لعنصر القائمة. تحدد المعلمات ملفNumberStyleaspose.words/numberstyle وتنسيق اختياري string يتم استخدامه عندCustom محدد .
type: docs
weight: 190
url: /ar/net/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel.GetEffectiveValue method

يبين تمثيل السلسلة لملف[`ListLevel`](../../listlevel) كائن index المحدد لعنصر القائمة. تحدد المعلمات ملف[`NumberStyle`](../../../aspose.words/numberstyle) وتنسيق اختياري string يتم استخدامه عندCustom محدد .

```csharp
public static string GetEffectiveValue(int index, NumberStyle numberStyle, 
    string customNumberStyleFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| index | Int32 | فهرس عنصر القائمة (يجب أن يكون في النطاق من 1 إلى 32767). |
| numberStyle | NumberStyle | ملف[`NumberStyle`](../../../aspose.words/numberstyle) التابع[`ListLevel`](../../listlevel) الكائن ._ x000d_ |
| customNumberStyleFormat | String | يتم استخدام سلسلة التنسيق الاختيارية عندماCustom محدد (على سبيل المثال "a، ç، ĝ، ...") ._ x000d_ في حالات أخرى ، يجب أن يكون هذا المعامل فارغًا أو فارغًا. |

### قيمة الإرجاع

تمثيل السلسلة لملف[`ListLevel`](../../listlevel) الكائن ، الموصوف بواسطة معلمة numberStyle و_ x000d_ معلمة customNumberStyleFormat ، في عنصر القائمة في الموضع الذي تحدده معلمة الفهرس.

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentException | customNumberStyleFormat يكون فارغًا أو فارغًا عندما يكون numberStyle مخصصًا. أو customNumberStyleFormat ليس فارغًا أو فارغًا عندما يكون numberStyle غير مخصص. أو customNumberStyleFormat غير صالح . |
| ArgumentOutOfRangeException | الفهرس خارج النطاق. |

### أمثلة

يوضح كيفية الحصول على التنسيق لقائمة بنمط الأرقام المخصص.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

// يمكننا الحصول على قيمة الفهرس المحدد لعنصر القائمة.
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### أنظر أيضا

* enum [NumberStyle](../../../aspose.words/numberstyle)
* class [ListLevel](../../listlevel)
* مساحة الاسم [Aspose.Words.Lists](../../listlevel)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->