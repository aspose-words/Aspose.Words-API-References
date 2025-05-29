---
title: CompositeNode.SelectSingleNode
linktitle: SelectSingleNode
articleTitle: SelectSingleNode
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تقوم طريقة SelectSingleNode الخاصة بـ CompositeNode باسترداد أول عقدة تطابق تعبير XPath الخاص بك بكفاءة للتعامل مع البيانات بشكل مبسط.
type: docs
weight: 220
url: /ar/net/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode.SelectSingleNode method

يحدد الأول[`Node`](../../node/) الذي يتطابق مع تعبير XPath.

```csharp
public Node SelectSingleNode(string xpath)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| xpath | String | تعبير XPath. |

### قيمة الإرجاع

الأول[`Node`](../../node/) الذي يتطابق مع استعلام XPath أو`باطل` إذا لم يتم العثور على عقدة مطابقة.

## ملاحظات

حاليًا، لا يُدعم سوى التعبيرات التي تحتوي على أسماء عناصر. التعبيرات التي تستخدم أسماء السمات غير مدعومة.

## أمثلة

يوضح كيفية تحديد عقد معينة باستخدام تعبير XPath.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// هذا التعبير سوف يستخرج جميع عقد الفقرات،
// والتي هي من نسل أي عقدة جدول في المستند.
NodeList nodeList = doc.SelectNodes("//الجدول//فقرة");

// قم بالتكرار خلال القائمة باستخدام مُعَدِّد وقم بطباعة محتويات كل فقرة في كل خلية من الجدول.
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// سيقوم هذا التعبير بتحديد أي فقرات تعتبر أبناءً مباشرين لأي عقدة نص في المستند.
nodeList = doc.SelectNodes("//النص/الفقرة");

//يمكننا التعامل مع القائمة كمصفوفة.
Assert.AreEqual(4, nodeList.ToArray().Length);

// استخدم SelectSingleNode لتحديد النتيجة الأولى لنفس التعبير المذكور أعلاه.
Node node = doc.SelectSingleNode("//النص/الفقرة");

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### أنظر أيضا

* class [Node](../../node/)
* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
