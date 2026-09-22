---
title: "Aspose::Words::Drawing::ShapeBase class"
linktitle: "ShapeBase"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ShapeBase class. الفئة الأساسية للكائنات في طبقة الرسم، مثل AutoShape، الشكل الحر، كائن OLE، عنصر تحكم ActiveX، أو صورة. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words.drawing/shapebase/
---
## ShapeBase class


الفئة الأساسية للكائنات في طبقة الرسم، مثل AutoShape أو شكل حر أو كائن OLE أو عنصر تحكم ActiveX أو صورة. لمعرفة المزيد، زر مقالة الوثائق [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class ShapeBase : public Aspose::Words::CompositeNode,
                  public Aspose::Words::IInline,
                  public Aspose::Words::Drawing::Core::IShape,
                  public Aspose::Words::IShapeAttrSource,
                  public Aspose::Words::Revisions::ITrackableNode,
                  public Aspose::Words::Drawing::Core::IFillable,
                  public Aspose::Words::Drawing::Core::IGlow,
                  public Aspose::Words::Drawing::Core::IReflection,
                  public Aspose::Words::Drawing::Core::ISoftEdge,
                  public Aspose::Words::Drawing::Core::IShadow
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| virtual [Accept](../../aspose.words/node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | يقبل زائرًا. |
| virtual [AcceptEnd](../../aspose.words/compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | عند تنفيذها في فئة مشتقة، تستدعي طريقة VisitXXXEnd لزائر المستند المحدد. |
| virtual [AcceptStart](../../aspose.words/compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | عند تنفيذها في فئة مشتقة، تستدعي طريقة VisitXXXStart لزائر المستند المحدد. |
| [AdjustWithEffects](./adjustwitheffects/)(System::Drawing::RectangleF) | يضيف إلى المستطيل المصدر قيم مدى التأثير ويعيد المستطيل النهائي. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | ينشئ نسخة مكررة من العقدة. |
| [get_AllowOverlap](./get_allowoverlap/)() | يحصل أو يضبط قيمة تحدد ما إذا كان هذا الشكل يمكنه التداخل مع أشكال أخرى. |
| [get_AlternativeText](./get_alternativetext/)() | يحدد النص البديل الذي يُعرض بدلاً من الرسم. |
| [get_AnchorLocked](./get_anchorlocked/)() | يحدد ما إذا كان مرساة الشكل مقفلة. |
| [get_AspectRatioLocked](./get_aspectratiolocked/)() | يحدد ما إذا كان نسبة أبعاد الشكل مقفلة. |
| [get_BehindText](./get_behindtext/)() | يحدد ما إذا كان الشكل أسفل أو أعلى النص. |
| [get_Bottom](./get_bottom/)() | يحصل على موضع الحافة السفلية للكتلة المحتوية على الشكل. |
| [get_Bounds](./get_bounds/)() | يحصل أو يضبط موقع وحجم الكتلة المحتوية على الشكل. |
| [get_BoundsInPoints](./get_boundsinpoints/)() | يحصل على موقع وحجم الكتلة المحتوية على الشكل بالنقاط، بالنسبة إلى مرساة الشكل الأعلى. |
| [get_BoundsWithEffects](./get_boundswitheffects/)() | يحصل على الامتداد النهائي لهذا الكائن الشكل بعد تطبيق تأثيرات الرسم. القيمة مقاسة بالنقاط. |
| [get_CanHaveImage](./get_canhaveimage/)() | يرجع **true** إذا كان نوع الشكل يسمح بوجود صورة. |
| [get_CoordOrigin](./get_coordorigin/)() | الإحداثيات في الزاوية العلوية اليسرى للكتلة المحتوية على هذا الشكل. |
| [get_CoordSize](./get_coordsize/)() | العرض والارتفاع لمساحة الإحداثيات داخل الكتلة المحتوية على هذا الشكل. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | يحصل على عدد الأطفال المباشرين لهذه العقدة. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | يحدد معرفًا مخصصًا للعقدة. |
| [get_DistanceBottom](./get_distancebottom/)() | يرجع أو يضبط المسافة (بالنقاط) بين نص المستند والحافة السفلية للشكل. |
| [get_DistanceLeft](./get_distanceleft/)() | يرجع أو يضبط المسافة (بالنقاط) بين نص المستند والحافة اليسرى للشكل. |
| [get_DistanceRight](./get_distanceright/)() | يرجع أو يضبط المسافة (بالنقاط) بين نص المستند والحافة اليمنى للشكل. |
| [get_DistanceTop](./get_distancetop/)() | يرجع أو يضبط المسافة (بالنقاط) بين نص المستند والحافة العلوية للشكل. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [get_Fill](./get_fill/)() | يحصل على تنسيق التعبئة للشكل. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | يحصل على الطفل الأول للعقدة. |
| [get_FlipOrientation](./get_fliporientation/)() | يبدل اتجاه الشكل. |
| [get_Font](./get_font/)() | يوفر الوصول إلى تنسيق الخط لهذا الكائن. |
| [get_Glow](./get_glow/)() | يحصل على تنسيق التوهج للشكل. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | يرجع **true** إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [get_Height](./get_height/)() | يحصل أو يضبط ارتفاع الكتلة المحتوية على الشكل. |
| [get_HeightRelative](./get_heightrelative/)() | الحصول أو تعيين القيمة التي تمثل نسبة الارتفاع النسبي للشكل. |
| [get_Hidden](./get_hidden/)() | الحصول أو تعيين قيمة منطقية تشير إلى ما إذا كان الشكل مرئيًا. |
| [get_HorizontalAlignment](./get_horizontalalignment/)() | يحدد كيفية تموضع الشكل أفقيًا. |
| [get_HRef](./get_href/)() | الحصول أو تعيين عنوان الارتباط الكامل للشكل. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | يرجع **true** لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [get_IsDecorative](./get_isdecorative/)() | الحصول أو تعيين العلامة التي تحدد ما إذا كان الشكل زخرفيًا في المستند. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | يرجع true إذا تم حذف هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsGroup](./get_isgroup/)() | إرجاع **true** إذا كان هذا شكل مجموعة. |
| [get_IsHorizontalRule](./get_ishorizontalrule/)() | إرجاع **true** إذا كان هذا الشكل قاعدة أفقية. |
| [get_IsImage](./get_isimage/)() | إرجاع **true** إذا كان هذا الشكل شكل صورة. |
| [get_IsInline](./get_isinline/)() | طريقة سريعة لتحديد ما إذا كان هذا الشكل موضعًا داخل النص. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | يرجع true إذا تم إدراج هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsLayoutInCell](./get_islayoutincell/)() | الحصول أو تعيين علامة تشير إلى ما إذا كان الشكل معروضًا داخل جدول أو خارجه. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | يرجع **true** إذا تم نقل (حذف) هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | يرجع **true** إذا تم نقل (إدراج) هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsSignatureLine](./get_issignatureline/)() | يشير إلى أن الشكل هو [SignatureLine](../signatureline/). |
| [get_IsTopLevel](./get_istoplevel/)() | إرجاع **true** إذا لم يكن هذا الشكل فرعًا لشكل مجموعة. |
| [get_IsWordArt](./get_iswordart/)() | إرجاع **true** إذا كان هذا الشكل كائن WordArt. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | يحصل على الطفل الأخير للعقدة. |
| [get_Left](./get_left/)() | الحصول أو تعيين موضع الحافة اليسرى للكتلة المحتوية على الشكل. |
| [get_LeftRelative](./get_leftrelative/)() | الحصول أو تعيين القيمة التي تمثل الموضع النسبي الأيسر للشكل بالنسبة المئوية. |
| [get_MarkupLanguage](./get_markuplanguage/)() const | الحصول على لغة الترميز المستخدمة لهذا الكائن الرسومي. |
| [get_Name](./get_name/)() | الحصول أو تعيين اسم الشكل الاختياري. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | يحصل على العقدة التي تلي هذه العقدة مباشرةً. |
| virtual [get_NodeType](../../aspose.words/node/get_nodetype/)() const | يحصل على نوع هذه العقدة. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | يحصل على الوالد المباشر لهذه العقدة. |
| [get_ParentParagraph](./get_parentparagraph/)() | إرجاع الفقرة الأصلية المباشرة. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | يرجع كائن [Range](../../aspose.words/range/) الذي يمثل الجزء من المستند الموجود داخل هذه العقدة. |
| [get_Reflection](./get_reflection/)() | الحصول على تنسيق الانعكاس للشكل. |
| [get_RelativeHorizontalPosition](./get_relativehorizontalposition/)() | يحدد بالنسبة إلى ماذا يتم تموضع الشكل أفقيًا. |
| [get_RelativeHorizontalSize](./get_relativehorizontalsize/)() | الحصول أو تعيين قيمة الحجم النسبي للشكل في الاتجاه الأفقي. |
| [get_RelativeVerticalPosition](./get_relativeverticalposition/)() | يحدد بالنسبة إلى ماذا يتم تموضع الشكل عموديًا. |
| [get_RelativeVerticalSize](./get_relativeverticalsize/)() | الحصول أو تعيين قيمة الحجم النسبي للشكل في الاتجاه العمودي. |
| [get_Right](./get_right/)() | الحصول على موضع الحافة اليمنى للكتلة المحتوية على الشكل. |
| [get_Rotation](./get_rotation/)() | يحدد الزاوية (بالدرجات) التي يتم تدوير الشكل بها. القيمة الإيجابية تتطابق مع زاوية الدوران في اتجاه عقارب الساعة. |
| [get_ScreenTip](./get_screentip/)() | يحدد النص المعروض عندما يتحرك مؤشر الفأرة فوق الشكل. |
| [get_ShadowFormat](./get_shadowformat/)() | يحصل على تنسيق الظل للشكل. |
| [get_ShapeType](./get_shapetype/)() | يحصل على نوع الشكل. |
| [get_SizeInPoints](./get_sizeinpoints/)() | يحصل على حجم الشكل بالنقاط. |
| [get_SoftEdge](./get_softedge/)() | يحصل على تنسيق الحافة الناعمة للشكل. |
| [get_Target](./get_target/)() | يحصل أو يضبط إطار الهدف لرابط الشكل. |
| [get_Title](./get_title/)() | يحصل أو يضبط العنوان (التسمية) لكائن الشكل الحالي. |
| [get_Top](./get_top/)() | يحصل أو يضبط موضع الحافة العلوية للكتلة المحتوية على الشكل. |
| [get_TopRelative](./get_toprelative/)() | يحصل أو يضبط القيمة التي تمثل الموضع العلوي النسبي للشكل بالنسبة المئوية. |
| [get_VerticalAlignment](./get_verticalalignment/)() | يحدد كيفية تموضع الشكل عمودياً. |
| [get_Width](./get_width/)() | يحصل أو يضبط عرض الكتلة المحتوية على الشكل. |
| [get_WidthRelative](./get_widthrelative/)() | يحصل أو يضبط القيمة التي تمثل نسبة عرض الشكل النسبي. |
| [get_WrapSide](./get_wrapside/)() | يحدد كيفية التفاف النص حول الشكل. |
| [get_WrapType](./get_wraptype/)() | يحدد ما إذا كان الشكل مضمناً أو عائمًا. بالنسبة للأشكال العائمة يحدد وضعية التفاف النص حول الشكل. |
| [get_ZOrder](./get_zorder/)() | يحدد ترتيب عرض الأشكال المتداخلة. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | يحصل على السلف الأول من النوع المحدد [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | يرجع عقدة الطفل رقم N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | يعيد مجموعة حية من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | يوفر دعمًا لتكرار نمط foreach على العقد الفرعية لهذا العقد. |
| [GetShapeRenderer](./getshaperenderer/)() | ينشئ ويعيد كائنًا يمكن استخدامه لتصوير هذا الشكل إلى صورة. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | يحصل على نص هذا العقد وجميع أطفاله. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يعيد فهرس العقدة الفرعية المحددة في مصفوفة العقد الفرعية. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [LocalToParent](./localtoparent/)(System::Drawing::PointF) | يحوّل قيمة من مساحة الإحداثيات المحلية إلى مساحة إحداثيات الشكل الأب. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على العقدة التالية وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | طريقة مساعدة تقوم بتحويل قيمة تعداد نوع العقدة إلى سلسلة صديقة للمستخدم. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من العنصر الأب. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | يزيل جميع العقد الفرعية للعقدة الحالية. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل جميع العقد التابعة لـ [SmartTag](../../aspose.words.markup/smarttag/) للعقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | يختار قائمة من العقد التي تطابق تعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | يختار أول [Node](../../aspose.words/node/) يطابق تعبير XPath. |
| [set_AllowOverlap](./set_allowoverlap/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_AllowOverlap](./get_allowoverlap/). |
| [set_AlternativeText](./set_alternativetext/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_AlternativeText](./get_alternativetext/). |
| [set_AnchorLocked](./set_anchorlocked/)(bool) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_AnchorLocked](./get_anchorlocked/). |
| [set_AspectRatioLocked](./set_aspectratiolocked/)(bool) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked](./get_aspectratiolocked/). |
| [set_BehindText](./set_behindtext/)(bool) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_BehindText](./get_behindtext/). |
| [set_Bounds](./set_bounds/)(System::Drawing::RectangleF) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_Bounds](./get_bounds/). |
| [set_CoordOrigin](./set_coordorigin/)(System::Drawing::Point) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_CoordOrigin](./get_coordorigin/). |
| [set_CoordSize](./set_coordsize/)(System::Drawing::Size) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_CoordSize](./get_coordsize/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DistanceBottom](./set_distancebottom/)(double) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_DistanceBottom](./get_distancebottom/). |
| [set_DistanceLeft](./set_distanceleft/)(double) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_DistanceLeft](./get_distanceleft/). |
| [set_DistanceRight](./set_distanceright/)(double) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_DistanceRight](./get_distanceright/). |
| [set_DistanceTop](./set_distancetop/)(double) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_DistanceTop](./get_distancetop/). |
| [set_FlipOrientation](./set_fliporientation/)(Aspose::Words::Drawing::FlipOrientation) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_FlipOrientation](./get_fliporientation/). |
| [set_Height](./set_height/)(double) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_Height](./get_height/). |
| [set_HeightRelative](./set_heightrelative/)(float) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_HeightRelative](./get_heightrelative/). |
| [set_Hidden](./set_hidden/)(bool) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_Hidden](./get_hidden/). |
| [set_HorizontalAlignment](./set_horizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment](./get_horizontalalignment/). |
| [set_HRef](./set_href/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_HRef](./get_href/). |
| [set_IsDecorative](./set_isdecorative/)(bool) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_IsDecorative](./get_isdecorative/). |
| [set_IsLayoutInCell](./set_islayoutincell/)(bool) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell](./get_islayoutincell/). |
| [set_Left](./set_left/)(double) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_Left](./get_left/). |
| [set_LeftRelative](./set_leftrelative/)(float) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_LeftRelative](./get_leftrelative/). |
| [set_Name](./set_name/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_Name](./get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalPosition](./set_relativehorizontalposition/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition](./get_relativehorizontalposition/). |
| [set_RelativeHorizontalSize](./set_relativehorizontalsize/)(Aspose::Words::Drawing::RelativeHorizontalSize) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize](./get_relativehorizontalsize/). |
| [set_RelativeVerticalPosition](./set_relativeverticalposition/)(Aspose::Words::Drawing::RelativeVerticalPosition) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition](./get_relativeverticalposition/). |
| [set_RelativeVerticalSize](./set_relativeverticalsize/)(Aspose::Words::Drawing::RelativeVerticalSize) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize](./get_relativeverticalsize/). |
| [set_Rotation](./set_rotation/)(double) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_Rotation](./get_rotation/). |
| [set_ScreenTip](./set_screentip/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_ScreenTip](./get_screentip/). |
| [set_Target](./set_target/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_Target](./get_target/). |
| [set_Title](./set_title/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_Title](./get_title/). |
| [set_Top](./set_top/)(double) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_Top](./get_top/). |
| [set_TopRelative](./set_toprelative/)(float) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_TopRelative](./get_toprelative/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment](./get_verticalalignment/). |
| [set_Width](./set_width/)(double) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_Width](./get_width/). |
| [set_WidthRelative](./set_widthrelative/)(float) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_WidthRelative](./get_widthrelative/). |
| [set_WrapSide](./set_wrapside/)(Aspose::Words::Drawing::WrapSide) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_WrapSide](./get_wrapside/). |
| [set_WrapType](./set_wraptype/)(Aspose::Words::Drawing::WrapType) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_WrapType](./get_wraptype/). |
| [set_ZOrder](./set_zorder/)(int32_t) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_ZOrder](./get_zorder/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | يصدّر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يصدّر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| static [Type](./type/)() |  |
## ملاحظات


هذه فئة مجردة. الفئتان المشتقتان اللتان يمكنك إنشاء كائنات منهما هما [Shape](../shape/) و [GroupShape](../groupshape/).

الشكل هو عقدة في شجرة المستند.

إذا كان الشكل طفلاً لكائن [Paragraph](../../aspose.words/paragraph/)، فإن الشكل يقال إنه "أعلى مستوى". تُقاس وتُحدد مواضع الأشكال ذات المستوى الأعلى بالنقاط.

يمكن أن يظهر الشكل أيضًا كطفل لكائن [GroupShape](../groupshape/) عندما يتم تجميع عدة أشكال. تُحدد مواضع الأشكال الفرعية لمجموعة الأشكال في مساحة الإحداثيات والوحدات التي تعرفها خصائص [CoordSize](./get_coordsize/) و [CoordOrigin](./get_coordorigin/) لمجموعة الأشكال الأصلية.

يمكن وضع الشكل مضمّنًا مع النص أو عائمًا. يتم التحكم في طريقة التموضع باستخدام خاصية [WrapType](./get_wraptype/).

عندما يكون الشكل عائمًا، يتم وضعه نسبةً إلى شيء ما (مثل الفقرة الحالية أو الهامش أو الصفحة). يتم تحديد التموضع النسبي للشكل باستخدام خصائص [RelativeHorizontalPosition](./get_relativehorizontalposition/) و [RelativeVerticalPosition](./get_relativeverticalposition/).

يمكن وضع الشكل العائم صراحةً باستخدام خصائص [Left](./get_left/) و [Top](./get_top/) أو محاذاته نسبةً إلى كائن آخر باستخدام خصائص [HorizontalAlignment](./get_horizontalalignment/) و [VerticalAlignment](./get_verticalalignment/).

## أمثلة



يوضح كيفية إدراج صورة عائمة في مركز الصفحة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج صورة عائمة ستظهر خلف النص المتداخل ووازنها إلى مركز الصفحة.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## انظر أيضًا

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
