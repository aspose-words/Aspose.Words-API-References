---
title: TxtSaveOptions.MaxCharactersPerLine
linktitle: MaxCharactersPerLine
articleTitle: MaxCharactersPerLine
second_title: Aspose.Words لـ .NET
description: اكتشف TxtSaveOptions MaxCharactersPerLine، حدّد بسهولة عدد الأحرف المسموح به في كل سطر لتحسين تنسيق النص. القيمة الافتراضية هي 0 لعدد غير محدود من الأحرف.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/txtsaveoptions/maxcharactersperline/
---
## TxtSaveOptions.MaxCharactersPerLine property

يحصل على أو يعين قيمة عددية تحدد الحد الأقصى لعدد الأحرف في كل سطر واحد. القيمة الافتراضية هي 0، وهذا يعني عدم وجود حد.

```csharp
public int MaxCharactersPerLine { get; set; }
```

## أمثلة

يوضح كيفية تعيين الحد الأقصى لعدد الأحرف في كل سطر.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// تعيين 30 حرفًا كحد أقصى مسموح به لكل سطر واحد.
TxtSaveOptions saveOptions = new TxtSaveOptions { MaxCharactersPerLine = 30 };

doc.Save(ArtifactsDir + "TxtSaveOptions.MaxCharactersPerLine.txt", saveOptions);
```

### أنظر أيضا

* class [TxtSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
