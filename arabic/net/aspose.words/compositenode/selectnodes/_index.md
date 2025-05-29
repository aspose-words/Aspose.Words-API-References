---
title: CompositeNode.SelectNodes
linktitle: SelectNodes
articleTitle: SelectNodes
second_title: Aspose.Words لـ .NET
description: استرداد العقد بسهولة باستخدام طريقة CompositeNode SelectNodes باستخدام تعبيرات XPath لتحسين معالجة البيانات وتبسيط الترميز.
type: docs
weight: 210
url: /ar/net/aspose.words/compositenode/selectnodes/
---
## CompositeNode.SelectNodes method

يحدد قائمة العقد المطابقة لتعبير XPath.

```csharp
public NodeList SelectNodes(string xpath)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| xpath | String | تعبير XPath. |

### قيمة الإرجاع

قائمة العقد المطابقة لاستعلام XPath.

## ملاحظات

حاليًا، لا يُدعم سوى التعبيرات التي تحتوي على أسماء عناصر. التعبيرات التي تستخدم أسماء السمات غير مدعومة.

## أمثلة

يوضح كيفية استخدام تعبير XPath لاختبار ما إذا كانت العقدة موجودة داخل حقل.

```csharp
Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

// ستحتوي NodeList الناتجة عن تعبير XPath هذا على جميع العقد التي نجدها داخل الحقل.
// ومع ذلك، يمكن أن تكون عقد FieldStart وFieldEnd موجودة في القائمة إذا كانت هناك حقول متداخلة في المسار.
// لا يتم حاليًا العثور على حقول نادرة حيث يمتد FieldCode أو FieldResult عبر فقرات متعددة.
NodeList resultList =
    doc.SelectNodes("//FieldStart/following-sibling::node()[following-sibling::FieldEnd]");

// تحقق مما إذا كان التشغيل المحدد هو أحد العقد الموجودة داخل الحقل.
Console.WriteLine($"Contents of the first Run node that's part of a field: {resultList.First(n => n.NodeType == NodeType.Run).GetText().Trim()}");
```

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

* class [NodeList](../../nodelist/)
* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
