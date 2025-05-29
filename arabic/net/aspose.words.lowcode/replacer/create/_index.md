---
title: Replacer.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تقوم طريقة Replacer Create بإنشاء مثيل جديد لمعالج الاستبدال الفعال لتحويل البيانات بسلاسة.
type: docs
weight: 10
url: /ar/net/aspose.words.lowcode/replacer/create/
---
## Replacer.Create method

ينشئ مثيلًا جديدًا لمعالج الاستبدال.

```csharp
public static Replacer Create(ReplacerContext context)
```

## أمثلة

يوضح كيفية استبدال السلسلة بـ regex في المستند باستخدام السياق.

```csharp
// هناك عدة طرق لاستبدال السلسلة بـ regex في المستند:
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

ReplacerContext replacerContext = new ReplacerContext();
replacerContext.SetReplacement(pattern, replacement);
replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

Replacer.Create(replacerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.ReplaceContextRegex.docx")
    .Execute();
```

يوضح كيفية استبدال السلسلة في المستند باستخدام السياق.

```csharp
// هناك عدة طرق لاستبدال السلسلة في المستند:
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

ReplacerContext replacerContext = new ReplacerContext();
replacerContext.SetReplacement(pattern, replacement);
replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

Replacer.Create(replacerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.ReplaceContext.docx")
    .Execute();
```

يوضح كيفية استبدال السلسلة في المستند باستخدام المستندات من التدفق باستخدام السياق.

```csharp
// هناك عدة طرق لاستبدال السلسلة في المستند باستخدام المستندات من الدفق:
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

using (FileStream streamIn = new FileStream(MyDir + "Footer.docx", FileMode.Open, FileAccess.Read))
{
    ReplacerContext replacerContext = new ReplacerContext();
    replacerContext.SetReplacement(pattern, replacement);
    replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceContextStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Create(replacerContext)
        .From(streamIn)
        .To(streamOut, SaveFormat.Docx)
        .Execute();
}
```

يوضح كيفية استبدال السلسلة بتعبير عادي في المستند باستخدام المستندات من التدفق باستخدام السياق.

```csharp
// هناك عدة طرق لاستبدال السلسلة بتعبير عادي في المستند باستخدام المستندات من التدفق:
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

using (FileStream streamIn = new FileStream(MyDir + "Replace regex.docx", FileMode.Open, FileAccess.Read))
{
    ReplacerContext replacerContext = new ReplacerContext();
    replacerContext.SetReplacement(pattern, replacement);
    replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceContextStreamRegex.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Create(replacerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### أنظر أيضا

* class [ReplacerContext](../../replacercontext/)
* class [Replacer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
