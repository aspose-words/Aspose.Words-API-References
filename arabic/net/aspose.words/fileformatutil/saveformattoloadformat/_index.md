---
title: FileFormatUtil.SaveFormatToLoadFormat
linktitle: SaveFormatToLoadFormat
articleTitle: SaveFormatToLoadFormat
second_title: Aspose.Words لـ .NET
description: حوّل ملفات SaveFormat بسهولة إلى LoadFormat باستخدام FileFormatUtil. بسّط إدارة الملفات وحسّن التوافق اليوم!
type: docs
weight: 90
url: /ar/net/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil.SaveFormatToLoadFormat method

يحول[`SaveFormat`](../../saveformat/) قيمة ل[`LoadFormat`](../../loadformat/) القيمة إذا كان ذلك ممكنا.

```csharp
public static LoadFormat SaveFormatToLoadFormat(SaveFormat saveFormat)
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentException | يرمي عندما لا يمكن التحويل. |

## أمثلة

يوضح كيفية تحويل تنسيق الحفظ إلى تنسيق التحميل المقابل له.

```csharp
Assert.AreEqual(LoadFormat.Html, FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Html));

// يمكن حفظ المستندات في بعض أنواع الملفات، ولكن لا يمكن تحميلها منها باستخدام Aspose.Words.
// إذا حاولنا تحويل تنسيق الحفظ من هذا النوع إلى تنسيق تحميل، فسيتم طرح استثناء.
Assert.Throws<ArgumentException>(() => FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Jpeg));
```

### أنظر أيضا

* enum [LoadFormat](../../loadformat/)
* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
