---
title: ListLevel.GetEffectiveValue
second_title: Aspose.Words لمراجع .NET API
description: ListLevel طريقة. يُبلغ عن تمثيل السلسلة لـListLevelكائن لـ Index المحدد لعنصر القائمة. تحدد المعلماتNumberStyle وتنسيق اختياري string يُستخدم متىCustom تم تحديده.
type: docs
weight: 190
url: /ar/net/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel.GetEffectiveValue method

يُبلغ عن تمثيل السلسلة لـ[`ListLevel`](../)كائن لـ Index المحدد لعنصر القائمة. تحدد المعلمات[`NumberStyle`](../../../aspose.words/numberstyle/) وتنسيق اختياري string يُستخدم متىCustom تم تحديده.

```csharp
public static string GetEffectiveValue(int index, NumberStyle numberStyle, 
    string customNumberStyleFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| index | Int32 | فهرس عنصر القائمة (يجب أن يكون في النطاق من 1 إلى 32767). |
| numberStyle | NumberStyle | ال[`NumberStyle`](../../../aspose.words/numberstyle/) التابع[`ListLevel`](../) الكائن. |
| customNumberStyleFormat | String | سلسلة التنسيق الاختيارية المستخدمة عندماCustom تم تحديده (على سبيل المثال "a, ç, ĝ, ..."). في حالات أخرى، يجب أن تكون هذه المعلمة`باطل` أو فارغ. |

### قيمة الإرجاع

تمثيل السلسلة لـ[`ListLevel`](../) الكائن الذي وصفه*numberStyle* المعلمة and و*customNumberStyleFormat* المعلمة، في عنصر القائمة في الموضع الذي يحدده*index* المعلمة.

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentException | *customNumberStyleFormat* يكون`باطل` أو فارغة عندما*numberStyle* مخصص.-أو- *customNumberStyleFormat* ليس`باطل` أو فارغة عندما*numberStyle* غير مخصص.-أو- *customNumberStyleFormat* غير صالح. |
| ArgumentOutOfRangeException | الفهرس خارج النطاق. |

### أمثلة

يوضح كيفية الحصول على تنسيق القائمة بنمط الأرقام المخصص.

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

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [ListLevel](../)
* مساحة الاسم [Aspose.Words.Lists](../../listlevel/)
* المجسم [Aspose.Words](../../../)


