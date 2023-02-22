---
title: Section.Body
second_title: Aspose.Words لمراجع .NET API
description: Section ملكية. إرجاع ملف الجسم العقدة الفرعية للقسم.
type: docs
weight: 20
url: /ar/net/aspose.words/section/body/
---
## Section.Body property

إرجاع ملف **الجسم** العقدة الفرعية للقسم.

```csharp
public Body Body { get; }
```

### ملاحظات

**الجسم** يحتوي على النص الرئيسي للقسم.

يعود فارغًا إذا لم يكن القسم يحتوي على ملف **الجسم** بين أبنائها.

### أمثلة

يمسح النص الرئيسي من جميع أقسام المستند مع ترك الأقسام نفسها.

```csharp
Document doc = new Document();

// يحتوي المستند الفارغ على قسم واحد وجسم واحد وفقرة واحدة.
// اتصل بطريقة "RemoveAllChildren" لإزالة كل هذه العقد ،
// وتنتهي بعقدة مستند بدون توابع.
doc.RemoveAllChildren();

// لا يحتوي هذا المستند الآن على عقد فرعية مركبة يمكننا إضافة محتوى إليها.
// إذا كنا نرغب في تعديله ، فسنحتاج إلى إعادة ملء مجموعة العقد الخاصة به.
// أولاً ، قم بإنشاء قسم جديد ، ثم قم بإلحاقه كعقدة فرعية بصفته فرعيًا.
Section section = new Section(doc);
doc.AppendChild(section);

// يحتاج القسم إلى جسم يحتوي على جميع محتوياته ويعرضها
// في الصفحة الواقعة بين رأس وتذييل القسم.
Body body = new Body(doc);
section.AppendChild(body);

// هذا الجسد ليس له أطفال ، لذا لا يمكننا إضافة أشواط إليه حتى الآن.
Assert.AreEqual(0, doc.FirstSection.Body.GetChildNodes(NodeType.Any, true).Count);

// اتصل بـ "WarrantyMinimum" للتأكد من أن هذا النص يحتوي على فقرة فارغة واحدة على الأقل. 
body.EnsureMinimum();

// الآن ، يمكننا إضافة عمليات التشغيل إلى النص ، والحصول على المستند لعرضها.
body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### أنظر أيضا

* class [Body](../../body/)
* class [Section](../)
* مساحة الاسم [Aspose.Words](../../section/)
* المجسم [Aspose.Words](../../../)


