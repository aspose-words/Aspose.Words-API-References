---
title: ListLevel.GetEffectiveValue
linktitle: GetEffectiveValue
articleTitle: GetEffectiveValue
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة ListLevel GetEffectiveValue لاسترجاع تمثيلات نصية لعناصر القائمة بسهولة. خصّصها باستخدام خيارات NumberStyle والتنسيق!
type: docs
weight: 190
url: /ar/net/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel.GetEffectiveValue method

يعرض التمثيل النصي لـ[`ListLevel`](../)كائن لـ index المحدد لعنصر القائمة. تحدد المعلمات[`NumberStyle`](../../../aspose.words/numberstyle/) وتنسيق اختياري string يستخدم عندCustom تم تحديده.

```csharp
public static string GetEffectiveValue(int index, NumberStyle numberStyle, 
    string customNumberStyleFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| index | Int32 | فهرس عنصر القائمة (يجب أن يكون في النطاق من 1 إلى 32767). |
| numberStyle | NumberStyle | ال[`NumberStyle`](../../../aspose.words/numberstyle/) التابع[`ListLevel`](../) الكائن. |
| customNumberStyleFormat | String | سلسلة التنسيق الاختيارية المستخدمة عندCustom يتم تحديد (على سبيل المثال "a, ç, ĝ, ..."). في حالات أخرى، يجب أن تكون هذه المعلمة`باطل` أو فارغ. |

### قيمة الإرجاع

التمثيل النصي لـ[`ListLevel`](../) الكائن الذي تم وصفه بواسطة*numberStyle* المعلمة and *customNumberStyleFormat* المعلمة، في عنصر القائمة في الموضع الذي تم تحديده بواسطة*index* المعلمة.

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentException | *customNumberStyleFormat* يكون`باطل` أو فارغة عندما*numberStyle* هو مخصص.-أو- *customNumberStyleFormat* ليس كذلك`باطل` أو فارغة عندما*numberStyle* غير مخصص.-أو- *customNumberStyleFormat* غير صالح. |
| ArgumentOutOfRangeException | المؤشر خارج النطاق. |

## أمثلة

يوضح كيفية الحصول على تنسيق القائمة باستخدام نمط الرقم المخصص.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

//يمكننا الحصول على قيمة للمؤشر المحدد لعنصر القائمة.
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### أنظر أيضا

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [ListLevel](../)
* مساحة الاسم [Aspose.Words.Lists](../../../aspose.words.lists/)
* المجسم [Aspose.Words](../../../)
