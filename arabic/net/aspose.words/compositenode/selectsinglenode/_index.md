---
title: CompositeNode.SelectSingleNode
second_title: Aspose.Words لمراجع .NET API
description: CompositeNode طريقة. تحديد الأولNode الذي يطابق تعبير XPath.
type: docs
weight: 220
url: /ar/net/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode.SelectSingleNode method

تحديد الأول[`Node`](../../node/) الذي يطابق تعبير XPath.

```csharp
public Node SelectSingleNode(string xpath)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| xpath | String | تعبير XPath |

### قيمة الإرجاع

الأول[`Node`](../../node/) الذي يطابق استعلام XPath أو`باطل` إذا لم يتم العثور على عقدة مطابقة.

### ملاحظات

يتم دعم التعبيرات التي تحتوي على أسماء العناصر فقط في الوقت الحالي. Expressions التي تستخدم أسماء السمات غير مدعومة.

### أمثلة

يوضح كيفية تحديد عقد معينة باستخدام تعبير XPath.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// هذا التعبير سوف يستخرج جميع عقد الفقرة،
// وهي من نسل أي عقدة جدول في المستند.
NodeList nodeList = doc.SelectNodes("//الجدول//الفقرة");

// كرر القائمة باستخدام العداد واطبع محتويات كل فقرة في كل خلية في الجدول.
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// سيحدد هذا التعبير أي فقرات تعتبر فرعية مباشرة لأي عقدة نص في المستند.
nodeList = doc.SelectNodes("//النص/الفقرة");

// يمكننا التعامل مع القائمة كمصفوفة.
Assert.AreEqual(4, nodeList.ToArray().Length);

// استخدم SelectSingleNode لتحديد النتيجة الأولى لنفس التعبير المذكور أعلاه.
Node node = doc.SelectSingleNode("//النص/الفقرة");

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### أنظر أيضا

* class [Node](../../node/)
* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../compositenode/)
* المجسم [Aspose.Words](../../../)


