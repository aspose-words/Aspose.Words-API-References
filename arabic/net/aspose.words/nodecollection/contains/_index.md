---
title: NodeCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تقوم طريقة NodeCollection Contains بالتحقق بكفاءة من وجود عقدة في مجموعتك، مما يعزز قدرات إدارة البيانات لديك.
type: docs
weight: 50
url: /ar/net/aspose.words/nodecollection/contains/
---
## NodeCollection.Contains method

يحدد ما إذا كانت العقدة موجودة في المجموعة.

```csharp
public bool Contains(Node node)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| node | Node | العقدة التي يجب تحديد موقعها. |

### قيمة الإرجاع

`حقيقي`إذا تم العثور على العنصر في المجموعة؛ وإلا،`خطأ شنيع`.

## ملاحظات

تقوم هذه الطريقة بإجراء بحث خطي؛ وبالتالي فإن متوسط وقت التنفيذ يتناسب مع[`Count`](../count/).

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
