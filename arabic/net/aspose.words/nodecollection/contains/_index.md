---
title: NodeCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words لـ .NET
description: NodeCollection Contains طريقة. تحديد ما إذا كانت العقدة موجودة في المجموعة في C#.
type: docs
weight: 50
url: /ar/net/aspose.words/nodecollection/contains/
---
## NodeCollection.Contains method

تحديد ما إذا كانت العقدة موجودة في المجموعة.

```csharp
public bool Contains(Node node)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| node | Node | العقدة لتحديد موقع. |

### قيمة الإرجاع

`حقيقي` إذا تم العثور على العنصر في المجموعة؛ خلاف ذلك،`خطأ شنيع`.

## ملاحظات

تقوم هذه الطريقة بإجراء بحث خطي؛ ولذلك فإن متوسط وقت التنفيذ يتناسب مع[`Count`](../count/).

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
