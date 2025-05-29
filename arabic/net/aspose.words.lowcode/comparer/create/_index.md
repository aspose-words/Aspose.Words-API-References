---
title: Comparer.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية استخدام طريقة Comparer Create بشكل فعال لإنشاء مثيلات جديدة لمعالج المحول لتحسين الأداء والكفاءة.
type: docs
weight: 10
url: /ar/net/aspose.words.lowcode/comparer/create/
---
## Create() {#create}

ينشئ مثيلًا جديدًا لمعالج المحول.

```csharp
public static Comparer Create()
```

### أنظر أيضا

* class [Comparer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Create(*[ComparerContext](../../comparercontext/)*) {#create_1}

ينشئ مثيلًا جديدًا لمعالج المقارنة.

```csharp
public static Comparer Create(ComparerContext context)
```

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

* class [ComparerContext](../../comparercontext/)
* class [Comparer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
