---
title: NodeList.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words لـ .NET
description: NodeList ToArray طريقة. نسخ كافة العقد من المجموعة إلى مجموعة جديدة من العقد في C#.
type: docs
weight: 40
url: /ar/net/aspose.words/nodelist/toarray/
---
## NodeList.ToArray method

نسخ كافة العقد من المجموعة إلى مجموعة جديدة من العقد.

```csharp
public Node[] ToArray()
```

### قيمة الإرجاع

مجموعة من العقد.

## ملاحظات

يجب ألا تقوم بإضافة/إزالة العقد أثناء التكرار عبر مجموعة من العقد لأن ذلك يبطل المكرِّر ويتطلب تحديثات للمجموعات المباشرة.

لتتمكن من إضافة/إزالة العقد أثناء التكرار، استخدم هذه الطريقة لنسخ العقد إلى مصفوفة ذات حجم ثابت ثم التكرار عبر المصفوفة.

## أمثلة

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
* class [NodeList](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
