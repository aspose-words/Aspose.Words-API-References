---
title: Shape Class
linktitle: Shape
articleTitle: Shape
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.Shape فصل. يمثل كائنًا في طبقة الرسم مثل الشكل التلقائي أو مربع النص أو الشكل الحر أو كائن OLE أو عنصر تحكم ActiveX أو الصورة في C#.
type: docs
weight: 1250
url: /ar/net/aspose.words.drawing/shape/
---
## Shape class

يمثل كائنًا في طبقة الرسم، مثل الشكل التلقائي، أو مربع النص، أو الشكل الحر، أو كائن OLE، أو عنصر تحكم ActiveX، أو الصورة.

لمعرفة المزيد، قم بزيارة[العمل مع الأشكال](https://docs.aspose.com/words/net/working-with-shapes/) مقالة توثيقية.

```csharp
public sealed class Shape : ShapeBase
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Shape](shape/)(*[DocumentBase](../../aspose.words/documentbase/), [ShapeType](../shapetype/)*) | إنشاء كائن شكل جديد. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AllowOverlap](../../aspose.words.drawing/shapebase/allowoverlap/) { get; set; } | الحصول على أو تعيين القيمة التي تحدد ما إذا كان هذا الشكل يمكن أن يتداخل مع الأشكال الأخرى. |
| [AlternativeText](../../aspose.words.drawing/shapebase/alternativetext/) { get; set; } | تحديد النص البديل الذي سيتم عرضه بدلاً من الرسم. |
| [AnchorLocked](../../aspose.words.drawing/shapebase/anchorlocked/) { get; set; } | يحدد ما إذا كان رابط الشكل مقفلاً أم لا. |
| [AspectRatioLocked](../../aspose.words.drawing/shapebase/aspectratiolocked/) { get; set; } | يحدد ما إذا كانت نسبة العرض إلى الارتفاع للشكل مقفلة أم لا. |
| [BehindText](../../aspose.words.drawing/shapebase/behindtext/) { get; set; } | يحدد ما إذا كان الشكل أسفل النص أو فوقه. |
| [Bottom](../../aspose.words.drawing/shapebase/bottom/) { get; } | الحصول على موضع الحافة السفلية للكتلة التي تحتوي على الشكل. |
| [Bounds](../../aspose.words.drawing/shapebase/bounds/) { get; set; } | الحصول على أو تعيين موقع وحجم الكتلة التي تحتوي على الشكل. |
| [BoundsInPoints](../../aspose.words.drawing/shapebase/boundsinpoints/) { get; } | الحصول على موقع وحجم الكتلة التي تحتوي على الشكل بالنقاط، بالنسبة إلى نقطة ارتساء الشكل العلوي. |
| [BoundsWithEffects](../../aspose.words.drawing/shapebase/boundswitheffects/) { get; } | الحصول على المدى النهائي لكائن الشكل هذا بعد تطبيق تأثيرات الرسم. يتم قياس القيمة بالنقاط. |
| [CanHaveImage](../../aspose.words.drawing/shapebase/canhaveimage/) { get; } | إرجاع`حقيقي` إذا كان نوع الشكل يسمح للشكل بأن يكون له صورة. |
| [Chart](../../aspose.words.drawing/shape/chart/) { get; } | يوفر الوصول إلى خصائص المخطط إذا كان هذا الشكل يحتوي على[`Chart`](../../aspose.words.drawing.charts/chart/) . |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | الإحداثيات في الزاوية العلوية اليسرى للكتلة التي تحتوي على هذا الشكل. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | عرض وارتفاع مساحة الإحداثيات داخل الكتلة المحتوية على هذا الشكل. |
| [Count](../../aspose.words/compositenode/count/) { get; } | يحصل على عدد الأطفال المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصصة. |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | إرجاع أو تعيين المسافة (بالنقاط) بين نص المستند والحافة السفلية للشكل. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | إرجاع أو تعيين المسافة (بالنقاط) بين نص المستند والحافة اليسرى للشكل. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | إرجاع أو تعيين المسافة (بالنقاط) بين نص المستند والحافة اليمنى للشكل. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | إرجاع أو تعيين المسافة (بالنقاط) بين نص المستند والحافة العلوية للشكل. |
| virtual [Document](../../aspose.words/node/document/) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة. |
| [ExtrusionEnabled](../../aspose.words.drawing/shape/extrusionenabled/) { get; } | إرجاع`حقيقي` إذا تم تمكين تأثير البثق. |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | الحصول على تنسيق التعبئة للشكل. |
| [FillColor](../../aspose.words.drawing/shape/fillcolor/) { get; set; } | يحدد لون الفرشاة الذي يملأ المسار المغلق للشكل. |
| [Filled](../../aspose.words.drawing/shape/filled/) { get; set; } | تحديد ما إذا كان سيتم ملء المسار المغلق للشكل أم لا. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | يحصل على الطفل الأول للعقدة. |
| [FirstParagraph](../../aspose.words.drawing/shape/firstparagraph/) { get; } | الحصول على الفقرة الأولى في الشكل. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | تبديل اتجاه الشكل. |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | يوفر الوصول إلى تنسيق الخط لهذا الكائن. |
| [HasChart](../../aspose.words.drawing/shape/haschart/) { get; } | إرجاع`حقيقي` اذا هذا`Shape` لديه[`Chart`](../../aspose.words.drawing.charts/chart/) . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [HasImage](../../aspose.words.drawing/shape/hasimage/) { get; } | إرجاع`حقيقي` إذا كان الشكل يحتوي على بايتات صورة أو يربط صورة. |
| [HasSmartArt](../../aspose.words.drawing/shape/hassmartart/) { get; } | إرجاع`حقيقي` اذا هذا`Shape` يحتوي على كائن SmartArt. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | الحصول على أو تعيين ارتفاع الكتلة التي تحتوي على الشكل. |
| [HeightRelative](../../aspose.words.drawing/shapebase/heightrelative/) { get; set; } | الحصول على أو تعيين القيمة التي تمثل النسبة المئوية للارتفاع النسبي للشكل. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | يحدد كيفية وضع الشكل أفقيًا. |
| [HorizontalRuleFormat](../../aspose.words.drawing/shape/horizontalruleformat/) { get; } | يوفر الوصول إلى خصائص شكل القاعدة الأفقية. بالنسبة للشكل الذي لا يمثل قاعدة أفقية، يتم إرجاعه`باطل` . |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | الحصول على عنوان الارتباط التشعبي الكامل للشكل أو تعيينه. |
| [ImageData](../../aspose.words.drawing/shape/imagedata/) { get; } | يوفر الوصول إلى صورة الشكل. إرجاع`باطل` إذا كان الشكل لا يمكن أن يحتوي على صورة. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع`حقيقي` لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [IsDecorative](../../aspose.words.drawing/shapebase/isdecorative/) { get; set; } | الحصول على أو تعيين العلامة التي تحدد ما إذا كان الشكل مزخرفًا في المستند. |
| [IsDeleteRevision](../../aspose.words.drawing/shapebase/isdeleterevision/) { get; } | إرجاع صحيح إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsGroup](../../aspose.words.drawing/shapebase/isgroup/) { get; } | إرجاع`حقيقي` إذا كان هذا شكل مجموعة. |
| [IsHorizontalRule](../../aspose.words.drawing/shapebase/ishorizontalrule/) { get; } | إرجاع`حقيقي` إذا كان هذا الشكل مسطرة أفقية. |
| [IsImage](../../aspose.words.drawing/shapebase/isimage/) { get; } | إرجاع`حقيقي` إذا كان هذا الشكل عبارة عن شكل صورة. |
| [IsInline](../../aspose.words.drawing/shapebase/isinline/) { get; } | طريقة سريعة لتحديد ما إذا كان هذا الشكل تم وضعه سطريًا مع النص. |
| [IsInsertRevision](../../aspose.words.drawing/shapebase/isinsertrevision/) { get; } | إرجاع صحيح إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsLayoutInCell](../../aspose.words.drawing/shapebase/islayoutincell/) { get; set; } | الحصول على أو تعيين علامة تشير إلى ما إذا كان الشكل معروضًا داخل الجدول أم خارجه. |
| [IsMoveFromRevision](../../aspose.words.drawing/shapebase/ismovefromrevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (حذفه) في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveToRevision](../../aspose.words.drawing/shapebase/ismovetorevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsSignatureLine](../../aspose.words.drawing/shapebase/issignatureline/) { get; } | يشير إلى أن الشكل هو أ[`SignatureLine`](../signatureline/) . |
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel/) { get; } | إرجاع`حقيقي`إذا لم يكن هذا الشكل تابعًا لشكل المجموعة. |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart/) { get; } | إرجاع`حقيقي` إذا كان هذا الشكل عبارة عن كائن WordArt. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | يحصل على الطفل الأخير للعقدة. |
| [LastParagraph](../../aspose.words.drawing/shape/lastparagraph/) { get; } | الحصول على الفقرة الأخيرة في الشكل. |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | الحصول على أو تعيين موضع الحافة اليسرى للكتلة التي تحتوي على الشكل. |
| [LeftRelative](../../aspose.words.drawing/shapebase/leftrelative/) { get; set; } | الحصول على أو تعيين القيمة التي تمثل الموضع الأيسر النسبي للشكل بالنسبة المئوية. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | يحصل على لغة الترميز المستخدمة لهذا الكائن الرسومي. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | الحصول على اسم الشكل الاختياري أو تعيينه. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.drawing/shape/nodetype/) { get; } | إرجاعShape . |
| [OleFormat](../../aspose.words.drawing/shape/oleformat/) { get; } | يوفر الوصول إلى بيانات OLE الخاصة بالشكل. بالنسبة للشكل الذي لا يعد كائن OLE أو عنصر تحكم ActiveX، يتم إرجاعه`باطل` . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الأصل المباشر لهذه العقدة. |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph/) { get; } | إرجاع الفقرة الأصلية المباشرة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ[`Range`](../../aspose.words/range/) الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition/) { get; set; } | يحدد نسبة إلى ما يتم وضعه أفقيًا. |
| [RelativeHorizontalSize](../../aspose.words.drawing/shapebase/relativehorizontalsize/) { get; set; } | الحصول على أو تعيين قيمة الحجم النسبي للشكل في الاتجاه الأفقي. |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition/) { get; set; } | يحدد نسبة إلى موضع الشكل عموديًا. |
| [RelativeVerticalSize](../../aspose.words.drawing/shapebase/relativeverticalsize/) { get; set; } | الحصول على أو تعيين قيمة الحجم النسبي للشكل في الاتجاه الرأسي. |
| [Right](../../aspose.words.drawing/shapebase/right/) { get; } | الحصول على موضع الحافة اليمنى للكتلة التي تحتوي على الشكل. |
| [Rotation](../../aspose.words.drawing/shapebase/rotation/) { get; set; } | تحدد الزاوية (بالدرجات) التي يتم تدوير الشكل بها. القيمة الموجبة تتوافق مع زاوية الدوران في اتجاه عقارب الساعة. |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip/) { get; set; } | تحديد النص المعروض عندما يتحرك مؤشر الماوس فوق الشكل. |
| [ShadowEnabled](../../aspose.words.drawing/shape/shadowenabled/) { get; } | إرجاع`حقيقي` إذا تم تمكين تأثير الظل. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | الحصول على تنسيق الظل للشكل. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | الحصول على نوع الشكل. |
| [SignatureLine](../../aspose.words.drawing/shape/signatureline/) { get; } | يحصل[`SignatureLine`](../signatureline/) كائن إذا كان الشكل عبارة عن خط توقيع. عائدات`باطل` وإلا. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | الحصول على حجم الشكل بالنقاط. |
| [StoryType](../../aspose.words.drawing/shape/storytype/) { get; } | إرجاعTextbox . |
| [Stroke](../../aspose.words.drawing/shape/stroke/) { get; } | يحدد حد الشكل. |
| [StrokeColor](../../aspose.words.drawing/shape/strokecolor/) { get; set; } | يحدد لون الحد. |
| [Stroked](../../aspose.words.drawing/shape/stroked/) { get; set; } | يحدد ما إذا كان سيتم تحديد المسار أم لا. |
| [StrokeWeight](../../aspose.words.drawing/shape/strokeweight/) { get; set; } | يحدد سمك الفرشاة الذي يحدد مسار الشكل بالنقاط. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | الحصول على الإطار المستهدف للارتباط التشعبي للشكل أو تعيينه. |
| [TextBox](../../aspose.words.drawing/shape/textbox/) { get; } | يحدد السمات التي تحدد كيفية عرض النص في الشكل. |
| [TextPath](../../aspose.words.drawing/shape/textpath/) { get; } | يحدد نص مسار النص (لكائن WordArt). |
| [Title](../../aspose.words.drawing/shapebase/title/) { get; set; } | الحصول على أو تعيين العنوان (التسمية التوضيحية) لكائن الشكل الحالي. |
| [Top](../../aspose.words.drawing/shapebase/top/) { get; set; } | الحصول على أو تعيين موضع الحافة العلوية للكتلة التي تحتوي على الشكل. |
| [TopRelative](../../aspose.words.drawing/shapebase/toprelative/) { get; set; } | الحصول على أو تعيين القيمة التي تمثل الموضع العلوي النسبي للشكل بالنسبة المئوية. |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment/) { get; set; } | يحدد كيفية وضع الشكل عموديًا. |
| [Width](../../aspose.words.drawing/shapebase/width/) { get; set; } | الحصول على أو تعيين عرض الكتلة التي تحتوي على الشكل. |
| [WidthRelative](../../aspose.words.drawing/shapebase/widthrelative/) { get; set; } | الحصول على أو تعيين القيمة التي تمثل النسبة المئوية للعرض النسبي للشكل. |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside/) { get; set; } | يحدد كيفية التفاف النص حول الشكل. |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype/) { get; set; } | يحدد ما إذا كان الشكل سطريًا أم عائمًا. للأشكال العائمة يحدد وضع الالتفاف للنص حول الشكل. |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder/) { get; set; } | تحديد ترتيب عرض الأشكال المتداخلة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.drawing/shape/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل الزائر. |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(*RectangleF*) | يضيف إلى قيم المستطيل المصدر لمدى التأثير ويعيد المستطيل النهائي. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../../aspose.words/node/)*) | إضافة العقدة المحددة إلى نهاية قائمة العقد التابعة لهذه العقدة. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | إنشاء نسخة مكررة من العقدة. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | إنشاء متصفح يمكن استخدامه لاجتياز العقد وقراءتها. |
| [FetchInheritedShapeAttr](../../aspose.words.drawing/shapebase/fetchinheritedshapeattr/)(*int*) | محجوز لاستخدام النظام. IShapeAttrSource. |
| [FetchShapeAttr](../../aspose.words.drawing/shapebase/fetchshapeattr/)(*int*) | محجوز لاستخدام النظام. IShapeAttrSource. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | يحصل على السلف الأول للمحدد[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | الحصول على السلف الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | إرجاع العقدة الفرعية N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | إرجاع مجموعة مباشرة من العقد الفرعية التي تطابق النوع المحدد. |
| [GetDirectShapeAttr](../../aspose.words.drawing/shapebase/getdirectshapeattr/)(*int*) | محجوز لاستخدام النظام. IShapeAttrSource. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | يوفر الدعم لتكرار كل نمط عبر العقد الفرعية لهذه العقدة. |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer/)() | إنشاء وإرجاع كائن يمكن استخدامه لتحويل هذا الشكل إلى صورة. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | الحصول على نص هذه العقدة وجميع أبنائها. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | إرجاع فهرس العقدة الفرعية المحددة في صفيف العقدة الفرعية. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | يقوم بإدراج العقدة المحددة مباشرة بعد العقدة المرجعية المحددة. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | يقوم بإدراج العقدة المحددة مباشرة قبل العقدة المرجعية المحددة. |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(*PointF*) | تحويل قيمة من المساحة الإحداثية المحلية إلى المساحة الإحداثية للشكل الأصلي. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../../aspose.words/node/)*) | إضافة العقدة المحددة إلى بداية قائمة العقد التابعة لهذه العقدة. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | إزالة جميع العقد الفرعية للعقدة الحالية. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../../aspose.words/node/)*) | إزالة العقدة الفرعية المحددة. |
| [RemoveShapeAttr](../../aspose.words.drawing/shapebase/removeshapeattr/)(*int*) | محجوز لاستخدام النظام. IShapeAttrSource. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag/)العقد التابعة للعقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | تحديد قائمة العقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | تحديد الأول[`Node`](../../aspose.words/node/) الذي يطابق تعبير XPath. |
| [SetShapeAttr](../../aspose.words.drawing/shapebase/setshapeattr/)(*int, object*) | محجوز لاستخدام النظام. IShapeAttrSource. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | تصدير محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | تصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| [UpdateSmartArtDrawing](../../aspose.words.drawing/shape/updatesmartartdrawing/)() | يقوم بتحديث رسم SmartArt المعروض مسبقًا باستخدام محرك العرض البارد SmartArt الخاص بـ Aspose.Words. |

## ملاحظات

باستخدام`Shape` يمكنك إنشاء أو تعديل الأشكال في مستند Microsoft Word.

خاصية مهمة للشكل هي[`ShapeType`](../shapebase/shapetype/)يمكن أن تحتوي الأشكال ذات الأنواع المختلفة على إمكانات مختلفة في مستند Word. على سبيل المثال، يمكن أن تحتوي الصور وأشكال OLE فقط على صور بداخلها. يمكن أن تحتوي معظم الأشكال على نص، ولكن ليس كلها.

الأشكال التي يمكن أن تحتوي على نص، يمكن أن تحتوي على[`Paragraph`](../../aspose.words/paragraph/) و [`Table`](../../aspose.words.tables/table/) العقد كأطفال.

## أمثلة

يوضح كيفية إدراج صورة عائمة في وسط الصفحة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل صورة عائمة ستظهر خلف النص المتداخل وقم بمحاذاتها مع منتصف الصفحة.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

يوضح كيفية استخراج الصور من مستند وحفظها في نظام الملفات المحلي كملفات فردية.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// احصل على مجموعة الأشكال من المستند،
// وحفظ بيانات الصورة لكل شكل مع صورة كملف في نظام الملفات المحلي.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // قد تحتوي بيانات صورة الأشكال على صور للعديد من تنسيقات الصور الممكنة.
        // يمكننا تحديد امتداد الملف لكل صورة تلقائيًا، بناءً على تنسيقها.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

يوضح كيفية حذف كافة الأشكال من مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل شكلين مع شكل مجموعة بداخله شكل آخر.
builder.InsertShape(ShapeType.Rectangle, 400, 200);
builder.InsertShape(ShapeType.Star, 300, 300);

GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 50, 200, 100);
group.CoordOrigin = new Point(-1000, -500);

Shape subShape = new Shape(doc, ShapeType.Cube);
subShape.Width = 500;
subShape.Height = 700;
subShape.Left = 0;
subShape.Top = 0;

group.AppendChild(subShape);
builder.InsertNode(group);

Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);

// قم بإزالة جميع عقد الشكل من المستند.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
shapes.Clear();

// اختفت جميع الأشكال، لكن شكل المجموعة لا يزال موجودًا في المستند.
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);

// قم بإزالة جميع أشكال المجموعة بشكل منفصل.
NodeCollection groupShapes = doc.GetChildNodes(NodeType.GroupShape, true);
groupShapes.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### أنظر أيضا

* class [ShapeBase](../shapebase/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
