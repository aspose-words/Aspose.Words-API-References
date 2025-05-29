---
title: NodeList.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words لـ .NET
description: كرر عملية NodeList بسهولة باستخدام دالة GetEnumerator. استمتع بوصول سهل وفعال إلى مجموعة عقدك بلغة C#.
type: docs
weight: 30
url: /ar/net/aspose.words/nodelist/getenumerator/
---
## NodeList.GetEnumerator method

يوفر تكرارًا بسيطًا بأسلوب "foreach" عبر مجموعة العقد.

```csharp
public IEnumerator<Node> GetEnumerator()
```

### قيمة الإرجاع

مُعَدِّد.

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
* class [NodeList](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
