---
title: Shape
second_title: Aspose.Words لمراجع .NET API
description: يمثل كائنًا في طبقة الرسم  مثل شكل تلقائي أو مربع نص أو شكل حر أو كائن OLE أو عنصر تحكم ActiveX أو صورة.
type: docs
weight: 1100
url: /ar/net/aspose.words.drawing/shape/
---
## Shape class

يمثل كائنًا في طبقة الرسم ، مثل شكل تلقائي أو مربع نص أو شكل حر أو كائن OLE أو عنصر تحكم ActiveX أو صورة.

```csharp
public sealed class Shape : ShapeBase
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Shape](shape/)(DocumentBase, ShapeType) | إنشاء كائن شكل جديد . |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AllowOverlap](../../aspose.words.drawing/shapebase/allowoverlap/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان هذا الشكل يمكن أن يتداخل مع الأشكال الأخرى. |
| [AlternativeText](../../aspose.words.drawing/shapebase/alternativetext/) { get; set; } | يحدد النص البديل الذي سيتم عرضه بدلاً من الرسم. |
| [AnchorLocked](../../aspose.words.drawing/shapebase/anchorlocked/) { get; set; } | يحدد ما إذا كانت نقطة ارتساء الشكل مؤمنة. |
| [AspectRatioLocked](../../aspose.words.drawing/shapebase/aspectratiolocked/) { get; set; } | يحدد ما إذا كانت نسبة العرض إلى الارتفاع للشكل مؤمنة. |
| [BehindText](../../aspose.words.drawing/shapebase/behindtext/) { get; set; } | تحديد ما إذا كان الشكل أسفل النص أو فوقه. |
| [Bottom](../../aspose.words.drawing/shapebase/bottom/) { get; } | الحصول على موضع الحافة السفلية للكتلة التي تحتوي على الشكل. |
| [Bounds](../../aspose.words.drawing/shapebase/bounds/) { get; set; } | الحصول على أو تحديد موقع وحجم الكتلة التي تحتوي على الشكل. |
| [BoundsInPoints](../../aspose.words.drawing/shapebase/boundsinpoints/) { get; } | الحصول على موقع وحجم الكتلة المحتوية للشكل بالنقاط ، بالنسبة إلى مرساة الشكل العلوي . |
| [BoundsWithEffects](../../aspose.words.drawing/shapebase/boundswitheffects/) { get; } | الحصول على المدى النهائي الذي يمتلكه كائن الشكل هذا بعد تطبيق تأثيرات الرسم. يتم قياس القيمة بالنقاط . |
| [CanHaveImage](../../aspose.words.drawing/shapebase/canhaveimage/) { get; } | إرجاع صحيح إذا كان نوع الشكل يسمح للشكل بأن يكون له صورة. |
| [Chart](../../aspose.words.drawing/shape/chart/) { get; } | يوفر الوصول إلى خصائص المخطط إذا كان هذا الشكل يحتوي على مخطط . |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | يحصل على جميع العقد الفرعية الفورية لهذه العقدة. |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | الإحداثيات الموجودة في الزاوية العلوية اليسرى للكتلة التي تحتوي على هذا الشكل. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | عرض وارتفاع مساحة الإحداثيات داخل الكتلة التي تحتوي على هذا الشكل . |
| [Count](../../aspose.words/compositenode/count/) { get; } | الحصول على عدد الأطفال المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص . |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | إرجاع أو تحديد المسافة (بالنقاط) بين نص المستند والحافة السفلية للشكل. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | إرجاع أو تحديد المسافة (بالنقاط) بين نص المستند والحافة اليسرى للشكل. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | إرجاع أو تحديد المسافة (بالنقاط) بين نص المستند والحافة اليمنى للشكل. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | إرجاع أو تحديد المسافة (بالنقاط) بين نص المستند والحافة العلوية للشكل. |
| virtual [Document](../../aspose.words/node/document/) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة . |
| [ExtrusionEnabled](../../aspose.words.drawing/shape/extrusionenabled/) { get; } | إرجاع صحيح إذا تم تمكين تأثير البثق. |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | الحصول على تنسيق التعبئة للشكل. |
| [FillColor](../../aspose.words.drawing/shape/fillcolor/) { get; set; } | يحدد لون الفرشاة الذي يملأ المسار المغلق للشكل. |
| [Filled](../../aspose.words.drawing/shape/filled/) { get; set; } | لتحديد ما إذا كان سيتم تعبئة المسار المغلق للشكل. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | الحصول على الطفل الأول للعقدة . |
| [FirstParagraph](../../aspose.words.drawing/shape/firstparagraph/) { get; } | الحصول على الفقرة الأولى بالشكل . |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | يبدل اتجاه الشكل. |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | يوفر الوصول إلى تنسيق خط هذا الكائن. |
| [HasChart](../../aspose.words.drawing/shape/haschart/) { get; } | يتم إرجاع صحيح إذا كان هذا الشكل يحتوي على ملف[`Chart`](./chart/) . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع صحيح إذا كانت هذه العقدة بها أي عقد فرعية. |
| [HasImage](../../aspose.words.drawing/shape/hasimage/) { get; } | إرجاع صحيح إذا كان للشكل بايت صورة أو ربط صورة. |
| [HasSmartArt](../../aspose.words.drawing/shape/hassmartart/) { get; } | إرجاع صحيح إذا كان هذا الشكل يحتوي على كائن SmartArt. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | الحصول على أو تحديد ارتفاع الكتلة التي تحتوي على الشكل. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | يحدد كيفية وضع الشكل أفقيًا. |
| [HorizontalRuleFormat](../../aspose.words.drawing/shape/horizontalruleformat/) { get; } | يوفر الوصول إلى خصائص شكل القاعدة الأفقية. بالنسبة للشكل الذي ليس قاعدة أفقية ، يتم إرجاع قيمة خالية. |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | الحصول على عنوان الارتباط التشعبي الكامل للشكل أو تعيينه. |
| [ImageData](../../aspose.words.drawing/shape/imagedata/) { get; } | يوفر الوصول إلى صورة الشكل. إرجاع فارغ إذا كان الشكل لا يمكن أن يحتوي على صورة . |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع صحيح لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [IsDecorative](../../aspose.words.drawing/shapebase/isdecorative/) { get; set; } | الحصول على أو تعيين العلامة التي تحدد ما إذا كان الشكل مزخرفًا في المستند. |
| [IsDeleteRevision](../../aspose.words.drawing/shapebase/isdeleterevision/) { get; } | إرجاع صحيح إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsGroup](../../aspose.words.drawing/shapebase/isgroup/) { get; } | إرجاع صحيح إذا كان هذا شكل مجموعة. |
| [IsHorizontalRule](../../aspose.words.drawing/shapebase/ishorizontalrule/) { get; } | إرجاع صحيح إذا كان هذا الشكل قاعدة أفقية. |
| [IsImage](../../aspose.words.drawing/shapebase/isimage/) { get; } | إرجاع صحيح إذا كان هذا الشكل هو شكل صورة. |
| [IsInline](../../aspose.words.drawing/shapebase/isinline/) { get; } | طريقة سريعة لتحديد ما إذا كان الشكل موضوعًا سطريًا مع النص. |
| [IsInsertRevision](../../aspose.words.drawing/shapebase/isinsertrevision/) { get; } | إرجاع صحيح إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsLayoutInCell](../../aspose.words.drawing/shapebase/islayoutincell/) { get; set; } | الحصول على أو تعيين علامة تشير إلى ما إذا كان الشكل معروضًا داخل جدول أو خارجه. |
| [IsMoveFromRevision](../../aspose.words.drawing/shapebase/ismovefromrevision/) { get; } | عوائد **حقيقي** إذا تم نقل (حذف) هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveToRevision](../../aspose.words.drawing/shapebase/ismovetorevision/) { get; } | عوائد **حقيقي** إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تعقب التغيير. |
| [IsSignatureLine](../../aspose.words.drawing/shapebase/issignatureline/) { get; } | يشير إلى أن الشكل عبارة عن خط توقيع. |
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel/) { get; } | إرجاع صحيح إذا لم يكن هذا الشكل فرعاً لشكل مجموعة . |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart/) { get; } | إرجاع صحيح إذا كان هذا الشكل عبارة عن كائن WordArt. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | الحصول على آخر تابع للعقدة . |
| [LastParagraph](../../aspose.words.drawing/shape/lastparagraph/) { get; } | الحصول على آخر فقرة بالشكل . |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | الحصول على أو تحديد موضع الحافة اليسرى للكتلة التي تحتوي على الشكل. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | Gets MarkupLanguage المستخدمة لهذا الكائن الرسومي. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | الحصول على اسم الشكل الاختياري أو تعيينه. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.drawing/shape/nodetype/) { get; } | عوائدShape . |
| [OleFormat](../../aspose.words.drawing/shape/oleformat/) { get; } | يوفر الوصول إلى بيانات OLE للشكل. بالنسبة لشكل ليس كائن OLE أو عنصر تحكم ActiveX ، يتم إرجاع قيمة خالية. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | الحصول على الأصل المباشر لهذه العقدة. |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph/) { get; } | إرجاع الفقرة الأصل المباشرة . |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ **نطاق** الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition/) { get; set; } | تحديد متعلق بالموضع الأفقي للشكل. |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition/) { get; set; } | تحديد متعلق بالموضع الرأسي للشكل. |
| [Right](../../aspose.words.drawing/shapebase/right/) { get; } | الحصول على موضع الحافة اليمنى للكتلة التي تحتوي على الشكل. |
| [Rotation](../../aspose.words.drawing/shapebase/rotation/) { get; set; } | يحدد الزاوية (بالدرجات) التي يتم تدوير الشكل بها. _ القيمة الموجبة تقابل زاوية الدوران في اتجاه عقارب الساعة . |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip/) { get; set; } | يحدد النص المعروض عندما يتحرك مؤشر الماوس فوق الشكل. |
| [ShadowEnabled](../../aspose.words.drawing/shape/shadowenabled/) { get; } | إرجاع صحيح إذا تم تمكين تأثير الظل. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | الحصول على تنسيق الظل للشكل . |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | يحصل على نوع الشكل. |
| [SignatureLine](../../aspose.words.drawing/shape/signatureline/) { get; } | يحصل[`SignatureLine`](./signatureline/) الكائن إذا كان الشكل عبارة عن خط توقيع. عائدات **لا شيء** خلاف ذلك. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | الحصول على حجم الشكل بالنقاط . |
| [StoryType](../../aspose.words.drawing/shape/storytype/) { get; } | عوائدTextbox . |
| [Stroke](../../aspose.words.drawing/shape/stroke/) { get; } | يحدد حد لشكل . |
| [StrokeColor](../../aspose.words.drawing/shape/strokecolor/) { get; set; } | يحدد لون ضربة الفرشاة . |
| [Stroked](../../aspose.words.drawing/shape/stroked/) { get; set; } | يحدد ما إذا كان سيتم تحديد المسار. |
| [StrokeWeight](../../aspose.words.drawing/shape/strokeweight/) { get; set; } | يحدد سماكة الفرشاة التي تضرب مسار الشكل بالنقاط. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | الحصول على أو تعيين الإطار الهدف للارتباط التشعبي للشكل. |
| [TextBox](../../aspose.words.drawing/shape/textbox/) { get; } | يحدد السمات التي تحدد كيفية عرض النص في شكل. |
| [TextPath](../../aspose.words.drawing/shape/textpath/) { get; } | يحدد نص مسار النص (لكائن WordArt) . |
| [Title](../../aspose.words.drawing/shapebase/title/) { get; set; } | الحصول على أو تعيين العنوان (التسمية التوضيحية) لكائن الشكل الحالي. |
| [Top](../../aspose.words.drawing/shapebase/top/) { get; set; } | الحصول على أو تحديد موضع الحافة العلوية للكتلة التي تحتوي على الشكل. |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment/) { get; set; } | يحدد كيفية وضع الشكل عموديًا. |
| [Width](../../aspose.words.drawing/shapebase/width/) { get; set; } | الحصول على أو تحديد عرض الكتلة التي تحتوي على الشكل. |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside/) { get; set; } | يحدد كيفية التفاف النص حول الشكل. |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype/) { get; set; } | يحدد ما إذا كان الشكل مضمنًا أم عائمًا. بالنسبة للأشكال العائمة ، يحدد وضع الالتفاف للنص حول الشكل. |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder/) { get; set; } | لتحديد ترتيب عرض الأشكال المتداخلة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.drawing/shape/accept/)(DocumentVisitor) | يقبل الزائر . |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(RectangleF) | يضيف إلى قيم مستطيل المصدر لمدى التأثير ويعيد المستطيل النهائي. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة . |
| [Clone](../../aspose.words/node/clone/)(bool) | لإنشاء نسخة مكررة من العقدة . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | محجوز لاستخدام النظام. IXPathNavigable. |
| [FetchInheritedShapeAttr](../../aspose.words.drawing/shapebase/fetchinheritedshapeattr/)(int) | محجوز لاستخدام النظام. IShapeAttrSource. |
| [FetchShapeAttr](../../aspose.words.drawing/shapebase/fetchshapeattr/)(int) | محجوز لاستخدام النظام. IShapeAttrSource. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | يحصل على أول سلف محدد[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | الحصول على الأصل الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | إرجاع العقدة الفرعية رقم N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | إرجاع مجموعة مباشرة من العقد الفرعية التي تطابق النوع المحدد. |
| [GetDirectShapeAttr](../../aspose.words.drawing/shapebase/getdirectshapeattr/)(int) | محجوز لاستخدام النظام. IShapeAttrSource. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | يوفر دعمًا لكل تكرار نمط على العقد التابعة لهذه العقدة . |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer/)() | إنشاء وإرجاع كائن يمكن استخدامه لتحويل هذا الشكل إلى صورة. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | يحصل على نص هذه العقدة وجميع توابعها. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | إرجاع فهرس العقدة الفرعية المحددة في مصفوفة العقدة الفرعية. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | يدخل العقدة المحددة مباشرة بعد العقدة المرجعية المحددة. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | يقوم بإدراج العقدة المحددة مباشرة قبل العقدة المرجعية المحددة. |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(PointF) | تحويل قيمة من مساحة الإحداثيات المحلية إلى مساحة إحداثيات الشكل الأصلي. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | يضيف العقدة المحددة إلى بداية قائمة العقد الفرعية لهذه العقدة . |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | يزيل كافة العقد التابعة للعقدة الحالية. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | يزيل العقدة الفرعية المحددة . |
| [RemoveShapeAttr](../../aspose.words.drawing/shapebase/removeshapeattr/)(int) | محجوز لاستخدام النظام. IShapeAttrSource. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag/) العقد التابعة للعقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | تحديد قائمة بالعقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | تحديد العقدة الأولى التي تطابق تعبير XPath. |
| [SetShapeAttr](../../aspose.words.drawing/shapebase/setshapeattr/)(int, object) | محجوز لاستخدام النظام. IShapeAttrSource. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | يصدر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| [UpdateSmartArtDrawing](../../aspose.words.drawing/shape/updatesmartartdrawing/)() | يحدّث رسم SmartArt الذي تم تقديمه مسبقًا باستخدام محرك العرض البارد Aspose.Words's SmartArt . |

### ملاحظات

باستخدام[`Shape`](./shape/) يمكنك إنشاء أو تعديل الأشكال في مستند Microsoft Word.

خاصية مهمة للشكل هو[`ShapeType`](../shapebase/shapetype/). يمكن أن تحتوي الأشكال ذات الأنواع المختلفة على إمكانيات مختلفة في مستند Word. على سبيل المثال ، يمكن أن تحتوي الصور فقط و OLE shape على صور بداخلها. يمكن أن تحتوي معظم الأشكال على نص ، ولكن ليس كلها.

يمكن أن تحتوي الأشكال التي يمكن أن تحتوي على نص[`Paragraph`](../../aspose.words/paragraph/) و [`Table`](../../aspose.words.tables/table/) العقد كأطفال.

### أمثلة

يوضح كيفية إدراج صورة عائمة في وسط الصفحة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل صورة عائمة ستظهر خلف النص المتداخل وقم بمحاذاة مركز الصفحة.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

يوضح كيفية استخراج الصور من مستند ، وحفظها في نظام الملفات المحلي كملفات فردية.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// احصل على مجموعة الأشكال من المستند ،
// وحفظ بيانات الصورة لكل شكل مع صورة كملف في نظام الملفات المحلي.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
        // قد تحتوي بيانات صور الأشكال على صور للعديد من تنسيقات الصور الممكنة. 
        // يمكننا تحديد امتداد ملف لكل صورة تلقائيًا ، بناءً على تنسيقها.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

يوضح كيفية حذف كل الأشكال من مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل شكلين مع شكل مجموعة مع شكل آخر بداخله.
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

// اختفت جميع الأشكال ، لكن شكل المجموعة لا يزال موجودًا في المستند.
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);

// قم بإزالة كافة أشكال المجموعة بشكل منفصل.
NodeCollection groupShapes = doc.GetChildNodes(NodeType.GroupShape, true);
groupShapes.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### أنظر أيضا

* class [ShapeBase](../shapebase/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
