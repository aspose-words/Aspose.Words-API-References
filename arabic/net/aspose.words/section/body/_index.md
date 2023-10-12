---
title: Section.Body
second_title: Aspose.Words لمراجع .NET API
description: Section ملكية. إرجاعBody العقدة الفرعية للقسم.
type: docs
weight: 20
url: /ar/net/aspose.words/section/body/
---
## Section.Body property

إرجاع[`Body`](../../body/) العقدة الفرعية للقسم.

```csharp
public Body Body { get; }
```

### ملاحظات

[`Body`](../../body/) يحتوي على النص الرئيسي للقسم.

عائدات`باطل` إذا لم يكن القسم[`Body`](../../body/) العقدة بين أبنائها.

### أمثلة

مسح النص الرئيسي من كافة أقسام المستند مع ترك الأقسام نفسها.

```csharp
Document doc = new Document();

// يحتوي المستند الفارغ على قسم واحد ونص واحد وفقرة واحدة.
// اتصل بالطريقة "RemoveAllChildren" لإزالة كل تلك العقد،
// وينتهي الأمر بعقدة مستند بدون أطفال.
doc.RemoveAllChildren();

// لا يحتوي هذا المستند الآن على عقد فرعية مركبة يمكننا إضافة محتوى إليها.
// إذا أردنا تعديله، فسنحتاج إلى إعادة ملء مجموعة العقد الخاصة به.
// أولاً، قم بإنشاء قسم جديد، ثم قم بإلحاقه كفرع لعقدة المستند الجذر.
Section section = new Section(doc);
doc.AppendChild(section);

// يحتاج القسم إلى نص يحتوي على جميع محتوياته ويعرضها
// في الصفحة الواقعة بين رأس القسم وتذييله.
Body body = new Body(doc);
section.AppendChild(body);

// هذا الجسم ليس له أطفال، لذا لا يمكننا إضافة عمليات تشغيل إليه بعد.
Assert.AreEqual(0, doc.FirstSection.Body.GetChildNodes(NodeType.Any, true).Count);

 // اتصل بـ "EnsureMinimum" للتأكد من أن هذا النص يحتوي على فقرة فارغة واحدة على الأقل.
body.EnsureMinimum();

// الآن، يمكننا إضافة عمليات تشغيل إلى النص والحصول على المستند لعرضها.
body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### أنظر أيضا

* class [Body](../../body/)
* class [Section](../)
* مساحة الاسم [Aspose.Words](../../section/)
* المجسم [Aspose.Words](../../../)


