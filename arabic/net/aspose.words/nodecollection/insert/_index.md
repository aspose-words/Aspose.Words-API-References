---
title: NodeCollection.Insert
linktitle: Insert
articleTitle: Insert
second_title: Aspose.Words لـ .NET
description: أدخل العقد بسهولة في NodeCollection الخاص بك عند أي فهرس باستخدام طريقة الإدراج المُبسّطة لدينا. حسّن إدارة بياناتك اليوم!
type: docs
weight: 80
url: /ar/net/aspose.words/nodecollection/insert/
---
## NodeCollection.Insert method

يقوم بإدراج عقدة في المجموعة عند الفهرس المحدد.

```csharp
public void Insert(int index, Node node)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| index | Int32 | الفهرس المبني على الصفر للعقدة. يُسمح بالمؤشرات السلبية وتشير إلى الوصول من نهاية القائمة. على سبيل المثال -1 يعني العقدة الأخيرة، -2 يعني العقدة الثانية قبل الأخيرة وهكذا. |
| node | Node | العقدة المراد إدراجها. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| NotSupportedException | ال[`NodeCollection`](../) هي مجموعة "عميقة". |

## ملاحظات

يتم إدراج العقدة كطفل في كائن العقدة الذي تم إنشاء المجموعة منه.

إذا كان المؤشر يساوي أو أكبر من[`Count`](../count/)، تتم إضافة العقدة في نهاية المجموعة.

إذا كان المؤشر سلبيًا وقيمته المطلقة أكبر من[`Count`](../count/)، تتم إضافة العقدة في نهاية المجموعة.

إذا تم إنشاء العقدة التي يتم إدراجها من مستند آخر، فيجب عليك استخدام [`ImportNode`](../../documentbase/importnode/) لاستيراد العقدة إلى المستند الحالي. يمكن بعد ذلك إدراج العقدة المستوردة في المستند الحالي.

## أمثلة

يوضح كيفية العمل مع NodeCollection.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإضافة نص إلى المستند عن طريق إدراج Runs باستخدام DocumentBuilder.
builder.Write("Run 1. ");
builder.Write("Run 2. ");

// كل استدعاء لطريقة "الكتابة" ينشئ عملية تشغيل جديدة،
// والتي تظهر بعد ذلك في RunCollection الخاصة بالفقرة الأصلية.
RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.AreEqual(2, runs.Count);

//يمكننا أيضًا إدراج عقدة في RunCollection يدويًا.
Run newRun = new Run(doc, "Run 3. ");
runs.Insert(3, newRun);

Assert.True(runs.Contains(newRun));
Assert.AreEqual("Run 1. Run 2. Run 3.", doc.GetText().Trim());

//الوصول إلى عمليات التشغيل الفردية وإزالتها لإزالة نصها من المستند.
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
