---
title: Shape Class
linktitle: Shape
articleTitle: Shape
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.Shape لإنشاء كائنات رسم متعددة الاستخدامات مثل الأشكال التلقائية ومربعات النص والصور بسهولة في مشاريعك.
type: docs
weight: 1640
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
| [Shape](shape/)(*[DocumentBase](../../aspose.words/documentbase/), [ShapeType](../shapetype/)*) | ينشئ كائن شكل جديد. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Adjustments](../../aspose.words.drawing/shape/adjustments/) { get; } | يوفر الوصول إلى قيم التعديل الخام لشكل ما. بالنسبة للشكل الذي لا يحتوي على أي قيم تعديل خام، فإنه يعيد مجموعة فارغة. |
| [AllowOverlap](../../aspose.words.drawing/shapebase/allowoverlap/) { get; set; } | يحصل على قيمة تحدد ما إذا كان هذا الشكل يمكنه التداخل مع الأشكال الأخرى أو يعينها. |
| [AlternativeText](../../aspose.words.drawing/shapebase/alternativetext/) { get; set; } | يحدد نصًا بديلًا ليتم عرضه بدلاً من الرسم البياني. |
| [AnchorLocked](../../aspose.words.drawing/shapebase/anchorlocked/) { get; set; } | يحدد ما إذا كان مرساة الشكل مقفلة. |
| [AspectRatioLocked](../../aspose.words.drawing/shapebase/aspectratiolocked/) { get; set; } | يحدد ما إذا كانت نسبة العرض إلى الارتفاع للشكل مقفلة. |
| [BehindText](../../aspose.words.drawing/shapebase/behindtext/) { get; set; } | يحدد ما إذا كان الشكل أسفل النص أم فوقه. |
| [Bottom](../../aspose.words.drawing/shapebase/bottom/) { get; } | يحصل على موضع الحافة السفلية للكتلة التي تحتوي على الشكل. |
| [Bounds](../../aspose.words.drawing/shapebase/bounds/) { get; set; } | يحصل على أو يعين موقع وحجم الكتلة التي تحتوي على الشكل. |
| [BoundsInPoints](../../aspose.words.drawing/shapebase/boundsinpoints/) { get; } | يحصل على موقع وحجم الكتلة التي تحتوي على الشكل بالنقاط، بالنسبة لمرساة الشكل الأعلى. |
| [BoundsWithEffects](../../aspose.words.drawing/shapebase/boundswitheffects/) { get; } | يحصل على المدى النهائي الذي أصبح عليه كائن الشكل هذا بعد تطبيق تأثيرات الرسم. يتم قياس القيمة بالنقاط. |
| [CanHaveImage](../../aspose.words.drawing/shapebase/canhaveimage/) { get; } | إرجاع`حقيقي` إذا كان نوع الشكل يسمح للشكل بالحصول على صورة. |
| [Chart](../../aspose.words.drawing/shape/chart/) { get; } | يوفر الوصول إلى خصائص الرسم البياني إذا كان هذا الشكل يحتوي على[`Chart`](../../aspose.words.drawing.charts/chart/) . |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | الإحداثيات في الزاوية العلوية اليسرى من الكتلة التي تحتوي على هذا الشكل. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | عرض وارتفاع مساحة الإحداثيات داخل الكتلة التي تحتوي على هذا الشكل. |
| [Count](../../aspose.words/compositenode/count/) { get; } | يحصل على عدد الأبناء المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص. |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | يقوم بإرجاع أو تعيين المسافة (بالنقاط) بين نص المستند والحافة السفلية للشكل. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | يقوم بإرجاع أو تعيين المسافة (بالنقاط) بين نص المستند والحافة اليسرى للشكل. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | يقوم بإرجاع أو تعيين المسافة (بالنقاط) بين نص المستند والحافة اليمنى للشكل. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | يقوم بإرجاع أو تعيين المسافة (بالنقاط) بين نص المستند والحافة العلوية للشكل. |
| virtual [Document](../../aspose.words/node/document/) { get; } | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [ExtrusionEnabled](../../aspose.words.drawing/shape/extrusionenabled/) { get; } | إرجاع`حقيقي` إذا تم تمكين تأثير البثق. |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | يحصل على تنسيق التعبئة للشكل. |
| [FillColor](../../aspose.words.drawing/shape/fillcolor/) { get; set; } | يحدد لون الفرشاة التي تملأ المسار المغلق للشكل. |
| [Filled](../../aspose.words.drawing/shape/filled/) { get; set; } | يحدد ما إذا كان سيتم ملء المسار المغلق للشكل. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | يحصل على أول طفل للعقدة. |
| [FirstParagraph](../../aspose.words.drawing/shape/firstparagraph/) { get; } | يحصل على الفقرة الأولى في الشكل. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | يقوم بتبديل اتجاه الشكل. |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | يوفر الوصول إلى تنسيق الخط لهذا الكائن. |
| [Glow](../../aspose.words.drawing/shapebase/glow/) { get; } | يحصل على تنسيق التوهج للشكل. |
| [HasChart](../../aspose.words.drawing/shape/haschart/) { get; } | إرجاع`حقيقي` إذا كان هذا`Shape` لديه[`Chart`](../../aspose.words.drawing.charts/chart/) . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [HasImage](../../aspose.words.drawing/shape/hasimage/) { get; } | إرجاع`حقيقي` إذا كان الشكل يحتوي على بايتات صورة أو روابط صورة. |
| [HasSmartArt](../../aspose.words.drawing/shape/hassmartart/) { get; } | إرجاع`حقيقي` إذا كان هذا`Shape` لديه كائن SmartArt. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | يحصل على ارتفاع الكتلة التي تحتوي على الشكل أو يعينه. |
| [HeightRelative](../../aspose.words.drawing/shapebase/heightrelative/) { get; set; } | يحصل على القيمة التي تمثل النسبة المئوية للارتفاع النسبي للشكل أو يعينها. |
| [Hidden](../../aspose.words.drawing/shapebase/hidden/) { get; set; } | يحصل على قيمة منطقية أو يعينها للإشارة إلى ما إذا كان الشكل مرئيًا أم لا. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | يحدد كيفية وضع الشكل أفقيًا. |
| [HorizontalRuleFormat](../../aspose.words.drawing/shape/horizontalruleformat/) { get; } | يوفر الوصول إلى خصائص شكل القاعدة الأفقية. بالنسبة للشكل الذي ليس قاعدة أفقية، يتم إرجاع`باطل` . |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | يحصل على عنوان الارتباط التشعبي الكامل لشكل ما أو يعينه. |
| [ImageData](../../aspose.words.drawing/shape/imagedata/) { get; } | يوفر الوصول إلى صورة الشكل. يعود`باطل` إذا لم يكن من الممكن أن يحتوي الشكل على صورة. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع`حقيقي` حيث يمكن لهذه العقدة أن تحتوي على عقد فرعية. |
| [IsDecorative](../../aspose.words.drawing/shapebase/isdecorative/) { get; set; } | يحصل على العلم الذي يحدد ما إذا كان الشكل مزخرفًا في المستند أم لا. |
| [IsDeleteRevision](../../aspose.words.drawing/shapebase/isdeleterevision/) { get; } | يعود صحيحًا إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsGroup](../../aspose.words.drawing/shapebase/isgroup/) { get; } | إرجاع`حقيقي` إذا كان هذا شكل المجموعة. |
| [IsHorizontalRule](../../aspose.words.drawing/shapebase/ishorizontalrule/) { get; } | إرجاع`حقيقي` إذا كان هذا الشكل عبارة عن مسطرة أفقية. |
| [IsImage](../../aspose.words.drawing/shapebase/isimage/) { get; } | إرجاع`حقيقي` إذا كان هذا الشكل هو شكل صورة. |
| [IsInline](../../aspose.words.drawing/shapebase/isinline/) { get; } | طريقة سريعة لتحديد ما إذا كان هذا الشكل موضوعًا في خط واحد مع النص. |
| [IsInsertRevision](../../aspose.words.drawing/shapebase/isinsertrevision/) { get; } | يعود صحيحًا إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsLayoutInCell](../../aspose.words.drawing/shapebase/islayoutincell/) { get; set; } | يحصل على علم أو يعينه للإشارة إلى ما إذا كان الشكل معروضًا داخل جدول أو خارجه. |
| [IsMoveFromRevision](../../aspose.words.drawing/shapebase/ismovefromrevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (حذفه) في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsMoveToRevision](../../aspose.words.drawing/shapebase/ismovetorevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsSignatureLine](../../aspose.words.drawing/shapebase/issignatureline/) { get; } | يشير إلى أن الشكل هو[`SignatureLine`](../signatureline/) . |
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel/) { get; } | إرجاع`حقيقي` إذا لم يكن هذا الشكل طفلاً لشكل المجموعة. |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart/) { get; } | إرجاع`حقيقي` إذا كان هذا الشكل عبارة عن كائن WordArt. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | يحصل على آخر طفل للعقدة. |
| [LastParagraph](../../aspose.words.drawing/shape/lastparagraph/) { get; } | يحصل على الفقرة الأخيرة في الشكل. |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | يحصل على موضع الحافة اليسرى للكتلة التي تحتوي على الشكل أو يعينه. |
| [LeftRelative](../../aspose.words.drawing/shapebase/leftrelative/) { get; set; } | يحصل على القيمة التي تمثل الموضع النسبي للشكل على اليسار كنسبة مئوية أو يعينها. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | يحصل على MarkupLanguage المستخدم لهذا الكائن الرسومي. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | يحصل على اسم الشكل الاختياري أو يعينه. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.drawing/shape/nodetype/) { get; } | إرجاعShape . |
| [OleFormat](../../aspose.words.drawing/shape/oleformat/) { get; } | يوفر الوصول إلى بيانات OLE الخاصة بالشكل. بالنسبة للشكل الذي ليس كائن OLE أو عنصر تحكم ActiveX، يُرجع`باطل` . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الوالد المباشر لهذه العقدة. |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph/) { get; } | إرجاع الفقرة الأصلية المباشرة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [Range](../../aspose.words/node/range/) { get; } | يعيد[`Range`](../../aspose.words/range/)الكائن الذي يمثل الجزء من المستند الموجود في هذه العقدة. |
| [Reflection](../../aspose.words.drawing/shapebase/reflection/) { get; } | يحصل على تنسيق الانعكاس للشكل. |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition/) { get; set; } | يحدد بالنسبة إلى ما يتم وضع الشكل أفقيًا. |
| [RelativeHorizontalSize](../../aspose.words.drawing/shapebase/relativehorizontalsize/) { get; set; } | يحصل على قيمة الحجم النسبي للشكل في الاتجاه الأفقي أو يعينها. |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition/) { get; set; } | يحدد بالنسبة إلى الوضع الرأسي للشكل. |
| [RelativeVerticalSize](../../aspose.words.drawing/shapebase/relativeverticalsize/) { get; set; } | يحصل على قيمة الحجم النسبي للشكل في الاتجاه الرأسي أو يعينها. |
| [Right](../../aspose.words.drawing/shapebase/right/) { get; } | يحصل على موضع الحافة اليمنى للكتلة التي تحتوي على الشكل. |
| [Rotation](../../aspose.words.drawing/shapebase/rotation/) { get; set; } | يحدد الزاوية (بالدرجات) التي يدور بها الشكل. القيمة الإيجابية تتوافق مع زاوية الدوران في اتجاه عقارب الساعة. |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip/) { get; set; } | يحدد النص المعروض عند تحرك مؤشر الماوس فوق الشكل. |
| [ShadowEnabled](../../aspose.words.drawing/shape/shadowenabled/) { get; } | إرجاع`حقيقي` إذا تم تمكين تأثير الظل. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | يحصل على تنسيق الظل للشكل. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | يحصل على نوع الشكل. |
| [SignatureLine](../../aspose.words.drawing/shape/signatureline/) { get; } | يحصل[`SignatureLine`](../signatureline/) الكائن إذا كان الشكل عبارة عن سطر توقيع. يُرجع`باطل` وإلا. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | يحصل على حجم الشكل بالنقاط. |
| [SoftEdge](../../aspose.words.drawing/shapebase/softedge/) { get; } | يحصل على تنسيق الحافة الناعمة للشكل. |
| [StoryType](../../aspose.words.drawing/shape/storytype/) { get; } | إرجاعTextbox . |
| [Stroke](../../aspose.words.drawing/shape/stroke/) { get; } | يحدد خطًا للشكل. |
| [StrokeColor](../../aspose.words.drawing/shape/strokecolor/) { get; set; } | يحدد لون الخط. |
| [Stroked](../../aspose.words.drawing/shape/stroked/) { get; set; } | يحدد ما إذا كان سيتم رسم المسار أم لا. |
| [StrokeWeight](../../aspose.words.drawing/shape/strokeweight/) { get; set; } | يحدد سمك الفرشاة التي ترسم مسار الشكل بالنقاط. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | يحصل على إطار الهدف لرابط الشكل التشعبي أو يعينه. |
| [TextBox](../../aspose.words.drawing/shape/textbox/) { get; } | يحدد السمات التي تحدد كيفية عرض النص في الشكل. |
| [TextPath](../../aspose.words.drawing/shape/textpath/) { get; } | يحدد نص مسار النص (لكائن WordArt). |
| [Title](../../aspose.words.drawing/shapebase/title/) { get; set; } | يحصل على عنوان (التعليق التوضيحي) لكائن الشكل الحالي أو يعينه. |
| [Top](../../aspose.words.drawing/shapebase/top/) { get; set; } | يحصل على موضع الحافة العلوية للكتلة التي تحتوي على الشكل أو يعينه. |
| [TopRelative](../../aspose.words.drawing/shapebase/toprelative/) { get; set; } | يحصل على القيمة التي تمثل الموضع العلوي النسبي للشكل كنسبة مئوية أو يعينها. |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment/) { get; set; } | يحدد كيفية وضع الشكل عموديًا. |
| [Width](../../aspose.words.drawing/shapebase/width/) { get; set; } | يحصل على عرض الكتلة التي تحتوي على الشكل أو يعينه. |
| [WidthRelative](../../aspose.words.drawing/shapebase/widthrelative/) { get; set; } | يحصل على القيمة التي تمثل النسبة المئوية للعرض النسبي للشكل أو يعينها. |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside/) { get; set; } | يحدد كيفية لف النص حول الشكل. |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype/) { get; set; } | يُحدد ما إذا كان الشكل مضمنًا أم عائمًا. بالنسبة للأشكال العائمة، يُحدد وضع التفاف النص حول الشكل. |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder/) { get; set; } | يحدد ترتيب عرض الأشكال المتداخلة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.drawing/shape/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل زائرًا. |
| override [AcceptEnd](../../aspose.words.drawing/shape/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل زائرًا لزيارة نهاية الشكل. |
| override [AcceptStart](../../aspose.words.drawing/shape/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل زائرًا لزيارة بداية الشكل. |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(*RectangleF*) | يضيف إلى قيم المستطيل المصدر لمدى التأثير ويعيد المستطيل النهائي. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | ينشئ نسخة مكررة من العقدة. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | ينشئ متصفحًا يمكن استخدامه للتنقل بين العقد وقراءتها. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | يحصل على السلف الأول للعنصر المحدد[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | يحصل على السلف الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | يعيد عقدة فرعية رقم N تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | يعيد مجموعة حية من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | يوفر الدعم لكل تكرار للأسلوب على العقد الفرعية لهذه العقدة. |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer/)() | ينشئ ويعيد كائنًا يمكن استخدامه لتحويل هذا الشكل إلى صورة. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | يحصل على نص هذه العقدة وجميع أبنائها. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | يعيد مؤشر العقدة الفرعية المحددة في مجموعة العقد الفرعية. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | يقوم بإدراج العقدة المحددة فورًا بعد عقدة المرجع المحددة. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | يقوم بإدراج العقدة المحددة مباشرة قبل عقدة المرجع المحددة. |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(*PointF*) | يحول قيمة من مساحة الإحداثيات المحلية إلى مساحة الإحداثيات للشكل الأصلي. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | يحصل على العقدة التالية وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | يضيف العقدة المحددة إلى بداية قائمة العقد الفرعية لهذه العقدة. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | يزيل جميع العقد الفرعية للعقدة الحالية. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | يزيل العقدة الفرعية المحددة. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag/) العقد المنحدرة من العقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | يحدد قائمة العقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | يحدد الأول[`Node`](../../aspose.words/node/) الذي يتطابق مع تعبير XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | يقوم بتصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| [UpdateSmartArtDrawing](../../aspose.words.drawing/shape/updatesmartartdrawing/)() | تحديث الرسم الذي تم تقديمه مسبقًا بتقنية SmartArt باستخدام محرك التقديم البارد SmartArt الخاص بـ Aspose.Words. |

## ملاحظات

باستخدام`Shape` باستخدام الفصل الدراسي، يمكنك إنشاء الأشكال أو تعديلها في مستند Microsoft Word.

من الخصائص المهمة للشكل هو[`ShapeType`](../shapebase/shapetype/)يمكن أن تحتوي الأشكال من أنواع مختلفة من x000d_ على إمكانيات مختلفة في مستند Word. على سبيل المثال، يمكن فقط للصور وأشكال OLE احتواء الصور بداخلها. يمكن لمعظم الأشكال احتواء النصوص، ولكن ليس جميعها.

الأشكال التي يمكن أن تحتوي على نص، يمكن أن تحتوي على[`Paragraph`](../../aspose.words/paragraph/) و [`Table`](../../aspose.words.tables/table/) العقد كأطفال.

## أمثلة

يوضح كيفية إدراج صورة عائمة في وسط الصفحة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج صورة عائمة ستظهر خلف النص المتداخل وقم بمحاذاتها مع مركز الصفحة.
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

// الحصول على مجموعة الأشكال من المستند،
// وحفظ بيانات الصورة لكل شكل مع الصورة كملف في نظام الملفات المحلي.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // قد تحتوي بيانات الصورة الخاصة بالأشكال على صور بتنسيقات صور متعددة محتملة.
        // يمكننا تحديد امتداد الملف لكل صورة تلقائيًا، استنادًا إلى تنسيقها.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

يوضح كيفية حذف كافة الأشكال من المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج شكلين مع شكل مجموعة يحتوي على شكل آخر بداخله.
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
