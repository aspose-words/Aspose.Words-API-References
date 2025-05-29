---
title: FileFormatInfo.HasMacros
linktitle: HasMacros
articleTitle: HasMacros
second_title: Aspose.Words لـ .NET
description: اكتشف ما إذا كان مستندك يتضمن وحدات ماكرو VBA باستخدام خاصية FileFormatInfo HasMacros. تمتع بأمان وفعالية مستندك اليوم!
type: docs
weight: 30
url: /ar/net/aspose.words/fileformatinfo/hasmacros/
---
## FileFormatInfo.HasMacros property

إرجاع`حقيقي` إذا كان هذا المستند يحتوي على وحدات ماكرو VBA.

```csharp
public bool HasMacros { get; }
```

## أمثلة

يوضح كيفية التحقق من وجود ماكرو VBA دون تحميل المستند.

```csharp
FileFormatInfo fileFormatInfo = FileFormatUtil.DetectFileFormat(MyDir + "Macro.docm");
Assert.IsTrue(fileFormatInfo.HasMacros);
```

### أنظر أيضا

* class [FileFormatInfo](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
