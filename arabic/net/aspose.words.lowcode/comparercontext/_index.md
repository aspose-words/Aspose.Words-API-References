---
title: ComparerContext Class
linktitle: ComparerContext
articleTitle: ComparerContext
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words LowCode ComparerContext لمقارنة المستندات بكفاءة، وتعزيز سير عملك من خلال التكامل السلس والميزات القوية.
type: docs
weight: 4220
url: /ar/net/aspose.words.lowcode/comparercontext/
---
## ComparerContext class

سياق مقارنة المستندات

```csharp
public class ComparerContext : ProcessorContext
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [ComparerContext](comparercontext/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AcceptRevisions](../../aspose.words.lowcode/comparercontext/acceptrevisions/) { get; set; } | يشير إلى ما إذا كان سيتم قبول المراجعات في المستندات قبل مقارنتها. إذا كانت المستندات المقارنة تحتوي على مراجعات وتم تعيين هذا العلم على "خطأ"، فسوف يرفض المعالج المراجعات. الإعداد الافتراضي هو`حقيقي` . |
| [Author](../../aspose.words.lowcode/comparercontext/author/) { get; set; } | المؤلف الذي سيتم تعيينه للمراجعات التي تم إنشاؤها أثناء مقارنة المستندات. |
| [CompareOptions](../../aspose.words.lowcode/comparercontext/compareoptions/) { get; } | الخيارات المستخدمة عند مقارنة المستندات. |
| [DateTime](../../aspose.words.lowcode/comparercontext/datetime/) { get; set; } | التاريخ والوقت المخصصين للمراجعات التي تم إنشاؤها أثناء مقارنة المستندات. |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | إعدادات الخط المستخدمة بواسطة المعالج. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | خيارات تخطيط المستند التي يستخدمها المعالج. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | استدعاء تحذيري يستخدمه المعالج. |

## أمثلة

يوضح كيفية مقارنة المستندات ببساطة باستخدام السياق.

```csharp
// هناك عدة طرق لمقارنة المستندات:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

ComparerContext comparerContext = new ComparerContext();
comparerContext.CompareOptions.IgnoreCaseChanges = true;
comparerContext.Author = "Author";
comparerContext.DateTime = new DateTime();

Comparer.Create(comparerContext)
    .From(firstDoc)
    .From(secondDoc)
    .To(ArtifactsDir + "LowCode.CompareContextDocuments.docx")
    .Execute();
```

يوضح كيفية مقارنة المستندات من التدفق باستخدام السياق.

```csharp
// هناك عدة طرق لمقارنة المستندات من التدفق:
using (FileStream firstStreamIn = new FileStream(MyDir + "Table column bookmarks.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Table column bookmarks.doc", FileMode.Open, FileAccess.Read))
    {
        ComparerContext comparerContext = new ComparerContext();
        comparerContext.CompareOptions.IgnoreCaseChanges = true;
        comparerContext.Author = "Author";
        comparerContext.DateTime = new DateTime();

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareContextStreamDocuments.docx", FileMode.Create, FileAccess.ReadWrite))
            Comparer.Create(comparerContext)
                .From(firstStreamIn)
                .From(secondStreamIn)
                .To(streamOut, SaveFormat.Docx)
                .Execute();
    }
}
```

### أنظر أيضا

* class [ProcessorContext](../processorcontext/)
* مساحة الاسم [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../)
