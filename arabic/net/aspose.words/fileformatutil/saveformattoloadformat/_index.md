---
title: FileFormatUtil.SaveFormatToLoadFormat
second_title: Aspose.Words لمراجع .NET API
description: FileFormatUtil طريقة. تحويل أSaveFormat القيمة إلى أLoadFormat القيمة إن أمكن.
type: docs
weight: 90
url: /ar/net/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil.SaveFormatToLoadFormat method

تحويل أ[`SaveFormat`](../../saveformat/) القيمة إلى أ[`LoadFormat`](../../loadformat/) القيمة إن أمكن.

```csharp
public static LoadFormat SaveFormatToLoadFormat(SaveFormat saveFormat)
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentException | يرمي عندما لا يمكن تحويل. |

### أمثلة

يوضح كيفية تحويل تنسيق الحفظ إلى تنسيق التحميل المقابل له.

```csharp
Assert.AreEqual(LoadFormat.Html, FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Html));

// يمكن أن تحتوي بعض أنواع الملفات على مستندات محفوظة فيها، لكن لا يمكن تحميلها باستخدام Aspose.Words.
// إذا حاولنا تحويل تنسيق حفظ من هذا النوع إلى تنسيق تحميل، فسيتم طرح استثناء.
Assert.Throws<ArgumentException>(() => FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Jpeg));
```

### أنظر أيضا

* enum [LoadFormat](../../loadformat/)
* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* مساحة الاسم [Aspose.Words](../../fileformatutil/)
* المجسم [Aspose.Words](../../../)


