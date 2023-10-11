---
title: Class OfficeMath
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Math.OfficeMath فصل. يمثل كائن Office Math مثل الدالة أو المعادلة أو المصفوفة أو ما شابه ذلك. يمكن أن تحتوي على العناصر الفرعية بما في ذلك مجموعة من النصوص الرياضية والإشارات المرجعية والتعليقات وغيرهاOfficeMathالمثيلات وبعض العقد الأخرى.
type: docs
weight: 4120
url: /ar/net/aspose.words.math/officemath/
---
## OfficeMath class

يمثل كائن Office Math مثل الدالة أو المعادلة أو المصفوفة أو ما شابه ذلك. يمكن أن تحتوي على العناصر الفرعية بما في ذلك مجموعة من النصوص الرياضية والإشارات المرجعية والتعليقات وغيرها`OfficeMath`المثيلات وبعض العقد الأخرى.

لمعرفة المزيد، قم بزيارة[العمل مع OfficeMath](https://docs.aspose.com/words/net/working-with-officemath/) مقالة توثيقية.

```csharp
public class OfficeMath : CompositeNode
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | يحصل على عدد الأطفال المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصصة. |
| [DisplayType](../../aspose.words.math/officemath/displaytype/) { get; set; } | الحصول على/تعيين نوع تنسيق عرض Office Math الذي يمثل ما إذا كانت المعادلة معروضة سطريًا مع text أو معروضة على السطر الخاص بها. |
| virtual [Document](../../aspose.words/node/document/) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | يحصل على الطفل الأول للعقدة. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع`حقيقي` لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [Justification](../../aspose.words.math/officemath/justification/) { get; set; } | الحصول على/تعيين مبررات Office Math. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | يحصل على الطفل الأخير للعقدة. |
| [MathObjectType](../../aspose.words.math/officemath/mathobjecttype/) { get; } | يحصل على النوع[`MathObjectType`](./mathobjecttype/) لكائن Office Math هذا. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.math/officemath/nodetype/) { get; } | إرجاعOfficeMath . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الأصل المباشر لهذه العقدة. |
| [ParentParagraph](../../aspose.words.math/officemath/parentparagraph/) { get; } | يسترد الأصل[`Paragraph`](../../aspose.words/paragraph/) من هذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ[`Range`](../../aspose.words/range/) الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.math/officemath/accept/)(DocumentVisitor) | يقبل الزائر. |
| override [AcceptEnd](../../aspose.words.math/officemath/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words.math/officemath/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | إنشاء نسخة مكررة من العقدة. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | إنشاء متصفح يمكن استخدامه لاجتياز العقد وقراءتها. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | يحصل على السلف الأول للمحدد[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | الحصول على السلف الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | إرجاع العقدة الفرعية N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | إرجاع مجموعة مباشرة من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | يوفر الدعم لتكرار كل نمط عبر العقد الفرعية لهذه العقدة. |
| [GetMathRenderer](../../aspose.words.math/officemath/getmathrenderer/)() | إنشاء وإرجاع كائن يمكن استخدامه لتحويل هذه المعادلة إلى صورة. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | الحصول على نص هذه العقدة وجميع أبنائها. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | إرجاع فهرس العقدة الفرعية المحددة في صفيف العقدة الفرعية. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | إزالة جميع العقد الفرعية للعقدة الحالية. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag/)العقد التابعة للعقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | تحديد قائمة العقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | تحديد الأول[`Node`](../../aspose.words/node/) الذي يطابق تعبير XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | تصدير محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | تصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

### ملاحظات

في هذا الإصدار من Aspose.Words،`OfficeMath` لا توفر العقد الأساليب العامة والخصائص لإنشاء أو تعديل ملف`OfficeMath` هدف. في هذا الإصدار، لا يمكنك إنشاء مثيل Math العقد أو تعديل الموجودة باستثناء حذفها.

`OfficeMath` لا يمكن إلا أن يكون طفلا[`Paragraph`](../../aspose.words/paragraph/).

### أمثلة

يوضح كيفية ضبط تنسيق عرض الرياضيات المكتبية.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// عقد OfficeMath التابعة لعقد OfficeMath الأخرى تكون دائمًا مضمّنة.
// العقدة التي نعمل معها هي العقدة الأساسية لتغيير موقعها ونوع العرض.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// تغيير الموقع ونوع العرض لعقدة OfficeMath.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### أنظر أيضا

* class [CompositeNode](../../aspose.words/compositenode/)
* مساحة الاسم [Aspose.Words.Math](../../aspose.words.math/)
* المجسم [Aspose.Words](../../)


