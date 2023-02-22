---
title: ListLevel.CustomNumberStyleFormat
second_title: Aspose.Words لمراجع .NET API
description: ListLevel ملكية. الحصول على تنسيق نمط الرقم المخصص لمستوى القائمة هذا. على سبيل المثال a ç ĝ ... .
type: docs
weight: 20
url: /ar/net/aspose.words.lists/listlevel/customnumberstyleformat/
---
## ListLevel.CustomNumberStyleFormat property

الحصول على تنسيق نمط الرقم المخصص لمستوى القائمة هذا. على سبيل المثال: "a، ç، ĝ، ..." .

```csharp
public string CustomNumberStyleFormat { get; }
```

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

* class [ListLevel](../)
* مساحة الاسم [Aspose.Words.Lists](../../listlevel/)
* المجسم [Aspose.Words](../../../)


