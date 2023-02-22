---
title: CompositeNode.SelectSingleNode
second_title: Aspose.Words لمراجع .NET API
description: CompositeNode طريقة. تحديد العقدة الأولى التي تطابق تعبير XPath.
type: docs
weight: 210
url: /ar/net/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode.SelectSingleNode method

تحديد العقدة الأولى التي تطابق تعبير XPath.

```csharp
public Node SelectSingleNode(string xpath)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| xpath | String | تعبير XPath. |

### قيمة الإرجاع

العقدة الأولى التي تطابق استعلام XPath أو فارغة إذا لم يتم العثور على عقدة مطابقة.

### ملاحظات

يتم دعم التعبيرات التي تحتوي على أسماء العناصر فقط في الوقت الحالي. لا يتم دعم Expressions التي تستخدم أسماء السمات.

### أمثلة

يوضح كيفية تحديد عقد معينة باستخدام تعبير XPath.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// هذا التعبير سوف يستخرج جميع عقد الفقرة ،
// التي تنحدر من أي عقدة جدول في المستند.
NodeList nodeList = doc.SelectNodes("// جدول // فقرة ") ;

// كرر من خلال القائمة باستخدام العداد واطبع محتويات كل فقرة في كل خلية من خلايا الجدول.
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// سيحدد هذا التعبير أي فقرات تكون فرعية مباشرة لأي عقدة أساسية في المستند.
nodeList = doc.SelectNodes("// نص / فقرة ") ;

// يمكننا التعامل مع القائمة كمصفوفة.
Assert.AreEqual(4, nodeList.ToArray().Length);

// استخدم SelectSingleNode لتحديد النتيجة الأولى لنفس التعبير على النحو الوارد أعلاه.
Node node = doc.SelectSingleNode("// نص / فقرة ") ;

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### أنظر أيضا

* class [Node](../../node/)
* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../compositenode/)
* المجسم [Aspose.Words](../../../)


