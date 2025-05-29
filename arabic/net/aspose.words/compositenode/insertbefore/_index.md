---
title: CompositeNode.InsertBefore
linktitle: InsertBefore
articleTitle: InsertBefore
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية استخدام طريقة CompositeNode InsertBefore لإدراج العقد بسلاسة قبل العقد المرجعية، مما يعزز إدارة بنية البيانات لديك.
type: docs
weight: 160
url: /ar/net/aspose.words/compositenode/insertbefore/
---
## CompositeNode.InsertBefore&lt;T&gt; method

يقوم بإدراج العقدة المحددة مباشرة قبل عقدة المرجع المحددة.

```csharp
public T InsertBefore<T>(T newChild, Node refChild)
    where T : Node
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| newChild | T | ال[`Node`](../../node/) لإدراج. |
| refChild | Node | ال[`Node`](../../node/) هذه هي العقدة المرجعية.*newChild* يتم وضعه قبل هذه العقدة. |

### قيمة الإرجاع

العقدة المدرجة.

## ملاحظات

لو*refChild* يكون`باطل` ، إدراجات*newChild* في نهاية قائمة العقد الفرعية.

إذا كان*newChild* إذا كان موجودًا بالفعل في الشجرة، فيجب إزالته أولاً.

إذا تم إنشاء العقدة التي يتم إدراجها من مستند آخر، فيجب عليك استخدام [`ImportNode`](../../documentbase/importnode/) لاستيراد العقدة إلى المستند الحالي. يمكن بعد ذلك إدراج العقدة المستوردة في المستند الحالي.

## أمثلة

يوضح كيفية إضافة وتحديث وحذف العقد الفرعية في مجموعة CompositeNode الفرعية.

```csharp
Document doc = new Document();

// تحتوي الوثيقة الفارغة، بشكل افتراضي، على فقرة واحدة.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// يمكن للعقد المركبة مثل فقرتنا أن تحتوي على عقد مركبة ومضمنة أخرى كأبناء.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// إنشاء ثلاث عقد تشغيل أخرى.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// لن يعرض نص المستند هذه العمليات حتى نقوم بإدخالها في عقدة مركبة
// وهذا في حد ذاته جزء من شجرة عقدة المستند، كما فعلنا في التشغيل الأول.
// يمكننا تحديد مكان محتوى النص للعقد التي نقوم بإدراجها
// يظهر في المستند عن طريق تحديد موقع الإدراج بالنسبة لعقدة أخرى في الفقرة.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

//أدخل التشغيل الثاني في الفقرة الموجودة أمام التشغيل الأولي.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

//أدخل التشغيل الثالث بعد التشغيل الأولي.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// قم بإدراج التشغيل الأول في بداية مجموعة العقد الفرعية للفقرة.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

//يمكننا تعديل محتويات التشغيل عن طريق تحرير وحذف العقد الفرعية الموجودة.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### أنظر أيضا

* class [Node](../../node/)
* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
