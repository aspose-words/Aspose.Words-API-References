---
title: NodeList.ToArray
second_title: Aspose.Words لمراجع .NET API
description: NodeList طريقة. ينسخ كل العقد من المجموعة إلى مصفوفة جديدة من العقد.
type: docs
weight: 40
url: /ar/net/aspose.words/nodelist/toarray/
---
## NodeList.ToArray method

ينسخ كل العقد من المجموعة إلى مصفوفة جديدة من العقد.

```csharp
public Node[] ToArray()
```

### قيمة الإرجاع

مجموعة من العقد.

### ملاحظات

يجب ألا تضيف / تزيل العقد أثناء التكرار على مجموعة من العقد لأنها تبطل المكرر وتتطلب تحديثات للمجموعات الحية.

لتتمكن من إضافة / إزالة العقد أثناء التكرار ، استخدم هذه الطريقة لنسخ عقد إلى مصفوفة ذات حجم ثابت ثم تكرارها عبر المصفوفة.

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
* class [NodeList](../)
* مساحة الاسم [Aspose.Words](../../nodelist/)
* المجسم [Aspose.Words](../../../)


