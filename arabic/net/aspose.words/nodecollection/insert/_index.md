---
title: NodeCollection.Insert
linktitle: Insert
articleTitle: Insert
second_title: Aspose.Words لـ .NET
description: NodeCollection Insert طريقة. إدراج عقدة في المجموعة في الفهرس المحدد في C#.
type: docs
weight: 80
url: /ar/net/aspose.words/nodecollection/insert/
---
## NodeCollection.Insert method

إدراج عقدة في المجموعة في الفهرس المحدد.

```csharp
public void Insert(int index, Node node)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| index | Int32 | الفهرس الصفري للعقدة. الفهارس السالبة مسموح بها وتشير إلى الوصول من الجزء الخلفي من القائمة. على سبيل المثال -1 يعني العقدة الأخيرة، -2 يعني الثانية قبل الأخيرة وهكذا. |
| node | Node | العقدة المراد إدراجها. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| NotSupportedException | ال[`NodeCollection`](../) هي مجموعة "عميقة". |

## ملاحظات

يتم إدراج العقدة كطفل في كائن العقدة الذي تم إنشاء المجموعة منه.

إذا كان المؤشر يساوي أو أكبر من[`Count`](../count/)، تتم إضافة العقدة في نهاية المجموعة.

إذا كان المؤشر سالباً وقيمته المطلقة أكبر من[`Count`](../count/)، تتم إضافة العقدة في نهاية المجموعة.

إذا تم إنشاء العقدة التي يتم إدراجها من مستند آخر، فيجب عليك استخدام [`ImportNode`](../../documentbase/importnode/) لاستيراد العقدة إلى المستند الحالي. يمكن بعد ذلك إدراج العقدة المستوردة في المستند الحالي.

## أمثلة

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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
