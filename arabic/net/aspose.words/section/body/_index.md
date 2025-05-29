---
title: Section.Body
linktitle: Body
articleTitle: Body
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية قسم الجسم التي تقوم باسترداد عقدة الجسم الفرعية، مما يعزز تطوير الويب الخاص بك من خلال إدارة المحتوى المبسطة.
type: docs
weight: 20
url: /ar/net/aspose.words/section/body/
---
## Section.Body property

يعيد[`Body`](../../body/) عقدة فرعية للقسم.

```csharp
public Body Body { get; }
```

## ملاحظات

[`Body`](../../body/) يحتوي على النص الرئيسي للقسم.

الإرجاعات`باطل` إذا لم يكن القسم يحتوي على[`Body`](../../body/) عقدة بين أبنائها.

## أمثلة

يقوم بمسح النص الرئيسي من كافة الأقسام في المستند مع ترك الأقسام نفسها.

```csharp
Document doc = new Document();

//تحتوي الوثيقة الفارغة على قسم واحد ونص واحد وفقرة واحدة.
//استدعاء طريقة "RemoveAllChildren" لإزالة كل هذه العقد،
// وينتهي الأمر بعقدة مستند بدون أطفال.
doc.RemoveAllChildren();

// لا تحتوي هذه الوثيقة الآن على أي عقد فرعية مركبة يمكننا إضافة محتوى إليها.
// إذا أردنا تحريره، فسوف نحتاج إلى إعادة ملء مجموعة العقد الخاصة به.
// أولاً، قم بإنشاء قسم جديد، ثم قم بإضافته كقسم فرعي إلى عقدة المستند الجذر.
Section section = new Section(doc);
doc.AppendChild(section);

// يحتاج القسم إلى نص، والذي سيحتوي على جميع محتوياته ويعرضها
// على الصفحة بين رأس القسم وتذييله.
Body body = new Body(doc);
section.AppendChild(body);

// هذا الجسم ليس له أطفال، لذلك لا يمكننا إضافة عمليات إليه بعد.
Assert.AreEqual(0, doc.FirstSection.Body.GetChildNodes(NodeType.Any, true).Count);

 // قم باستدعاء "EnsureMinimum" للتأكد من أن هذا النص يحتوي على فقرة فارغة واحدة على الأقل.
body.EnsureMinimum();

// الآن، يمكننا إضافة عمليات تشغيل إلى النص، والحصول على المستند لعرضها.
body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### أنظر أيضا

* class [Body](../../body/)
* class [Section](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
