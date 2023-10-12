---
title: NodeCollection.Remove
second_title: Aspose.Words لمراجع .NET API
description: NodeCollection طريقة. إزالة العقدة من المجموعة ومن المستند.
type: docs
weight: 90
url: /ar/net/aspose.words/nodecollection/remove/
---
## NodeCollection.Remove method

إزالة العقدة من المجموعة ومن المستند.

```csharp
public void Remove(Node node)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| node | Node | العقدة المراد إزالتها. |

### أمثلة

يوضح كيفية العمل مع NodeCollection.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أضف نصًا إلى المستند عن طريق إدراج عمليات التشغيل باستخدام DocumentBuilder.
builder.Write("Run 1. ");
builder.Write("Run 2. ");

// كل استدعاء لأسلوب "الكتابة" يُنشئ عملية تشغيل جديدة،
// والذي يظهر بعد ذلك في RunCollection الخاص بالفقرة الأصلية.
RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.AreEqual(2, runs.Count);

// يمكننا أيضًا إدراج عقدة في RunCollection يدويًا.
Run newRun = new Run(doc, "Run 3. ");
runs.Insert(3, newRun);

Assert.True(runs.Contains(newRun));
Assert.AreEqual("Run 1. Run 2. Run 3.", doc.GetText().Trim());

// الوصول إلى عمليات التشغيل الفردية وإزالتها لإزالة النص الخاص بها من المستند.
Run run = runs[1];
runs.Remove(run);

Assert.AreEqual("Run 1. Run 3.", doc.GetText().Trim());
Assert.NotNull(run);
Assert.False(runs.Contains(run));
```

### أنظر أيضا

* class [Node](../../node/)
* class [NodeCollection](../)
* مساحة الاسم [Aspose.Words](../../nodecollection/)
* المجسم [Aspose.Words](../../../)


