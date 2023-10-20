---
title: ListLevel.CustomNumberStyleFormat
linktitle: CustomNumberStyleFormat
articleTitle: CustomNumberStyleFormat
second_title: Aspose.Words لـ .NET
description: ListLevel CustomNumberStyleFormat ملكية. الحصول على تنسيق نمط الأرقام المخصص لمستوى القائمة هذا. على سبيل المثال أ ç ĝ  في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.lists/listlevel/customnumberstyleformat/
---
## ListLevel.CustomNumberStyleFormat property

الحصول على تنسيق نمط الأرقام المخصص لمستوى القائمة هذا. على سبيل المثال: "أ، ç، ĝ، ...".

```csharp
public string CustomNumberStyleFormat { get; }
```

## أمثلة

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

* class [ListLevel](../)
* مساحة الاسم [Aspose.Words.Lists](../../../aspose.words.lists/)
* المجسم [Aspose.Words](../../../)
