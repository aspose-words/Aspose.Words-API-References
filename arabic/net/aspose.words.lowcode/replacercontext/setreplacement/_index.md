---
title: ReplacerContext.SetReplacement
linktitle: SetReplacement
articleTitle: SetReplacement
second_title: Aspose.Words لـ .NET
description: قم بتعزيز عمليات البحث والاستبدال باستخدام طريقة ReplacerContext SetReplacement، مما يسمح بإدارة النمط والاستبدال بشكل سلس لتحقيق الكفاءة.
type: docs
weight: 30
url: /ar/net/aspose.words.lowcode/replacercontext/setreplacement/
---
## SetReplacement(*string, string*) {#setreplacement}

يحدد النمط والاستبدال المستخدم في عملية البحث/الاستبدال.

```csharp
public void SetReplacement(string pattern, string replacement)
```

## ملاحظات

يؤدي استخدام هذه الطريقة إلى إلغاء النمط والاستبدال المحددين مسبقًا.

## أمثلة

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

### أنظر أيضا

* class [ReplacerContext](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## SetReplacement(*Regex, string*) {#setreplacement_1}

يحدد النمط والاستبدال المستخدم في عملية البحث/الاستبدال.

```csharp
public void SetReplacement(Regex pattern, string replacement)
```

## ملاحظات

يؤدي استخدام هذه الطريقة إلى إلغاء النمط والاستبدال المحددين مسبقًا.

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

* class [ReplacerContext](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
