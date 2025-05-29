---
title: ReplacerContext Class
linktitle: ReplacerContext
articleTitle: ReplacerContext
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words LowCode ReplacerContext لإجراء عمليات بحث واستبدال سلسة، مما يعزز أتمتة مستنداتك وكفاءتها.
type: docs
weight: 4350
url: /ar/net/aspose.words.lowcode/replacercontext/
---
## ReplacerContext class

سياق عملية البحث/الاستبدال.

```csharp
public class ReplacerContext : ProcessorContext
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [ReplacerContext](replacercontext/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [FindReplaceOptions](../../aspose.words.lowcode/replacercontext/findreplaceoptions/) { get; } | خيارات البحث/الاستبدال. |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | إعدادات الخط المستخدمة بواسطة المعالج. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | خيارات تخطيط المستند التي يستخدمها المعالج. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | استدعاء تحذيري يستخدمه المعالج. |

## طُرق

| اسم | وصف |
| --- | --- |
| [SetReplacement](../../aspose.words.lowcode/replacercontext/setreplacement/#setreplacement_1)(*Regex, string*) | يحدد النمط والاستبدال المستخدم في عملية البحث/الاستبدال. |
| [SetReplacement](../../aspose.words.lowcode/replacercontext/setreplacement/#setreplacement)(*string, string*) | يحدد النمط والاستبدال المستخدم في عملية البحث/الاستبدال. |

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

* class [ProcessorContext](../processorcontext/)
* مساحة الاسم [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../)
