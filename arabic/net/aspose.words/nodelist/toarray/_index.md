---
title: NodeList.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words لـ .NET
description: قم بتحويل NodeList إلى مصفوفة بسهولة باستخدام طريقة ToArray، مما يبسط معالجة العقد ويعزز سير عمل تطوير الويب الخاص بك.
type: docs
weight: 40
url: /ar/net/aspose.words/nodelist/toarray/
---
## NodeList.ToArray method

نسخ جميع العقد من المجموعة إلى مجموعة جديدة من العقد.

```csharp
public Node[] ToArray()
```

### قيمة الإرجاع

مجموعة من العقد.

## ملاحظات

لا يجب عليك إضافة/إزالة العقد أثناء التكرار عبر مجموعة من العقد لأن ذلك يبطل عمل المتكرر ويتطلب تحديثات للمجموعات الحية.

لتتمكن من إضافة/إزالة العقد أثناء التكرار، استخدم هذه الطريقة لنسخ عقد إلى مصفوفة ذات حجم ثابت ثم التكرار عبر المصفوفة.

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
