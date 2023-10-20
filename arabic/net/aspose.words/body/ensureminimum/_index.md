---
title: Body.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words لـ .NET
description: Body EnsureMinimum طريقة. إذا لم يكن العنصر الفرعي الأخير فقرة فسيتم إنشاء فقرة واحدة فارغة وإلحاقها في C#.
type: docs
weight: 50
url: /ar/net/aspose.words/body/ensureminimum/
---
## Body.EnsureMinimum method

إذا لم يكن العنصر الفرعي الأخير فقرة، فسيتم إنشاء فقرة واحدة فارغة وإلحاقها.

```csharp
public void EnsureMinimum()
```

## أمثلة

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

* class [Body](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
