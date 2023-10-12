---
title: TxtSaveOptions.MaxCharactersPerLine
second_title: Aspose.Words لمراجع .NET API
description: TxtSaveOptions ملكية. الحصول على أو تعيين قيمة عددية تحدد الحد الأقصى لعدد الأحرف في سطر واحد. القيمة الافتراضية هي 0 وهذا يعني عدم وجود حد.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/txtsaveoptions/maxcharactersperline/
---
## TxtSaveOptions.MaxCharactersPerLine property

الحصول على أو تعيين قيمة عددية تحدد الحد الأقصى لعدد الأحرف في سطر واحد. القيمة الافتراضية هي 0، وهذا يعني عدم وجود حد.

```csharp
public int MaxCharactersPerLine { get; set; }
```

### أمثلة

يوضح كيفية تعيين الحد الأقصى لعدد الأحرف في كل سطر.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// قم بتعيين 30 حرفًا كحد أقصى مسموح به لكل سطر واحد.
TxtSaveOptions saveOptions = new TxtSaveOptions { MaxCharactersPerLine = 30 };

doc.Save(ArtifactsDir + "TxtSaveOptions.MaxCharactersPerLine.txt", saveOptions);
```

### أنظر أيضا

* class [TxtSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../txtsaveoptions/)
* المجسم [Aspose.Words](../../../)


