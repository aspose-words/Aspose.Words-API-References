---
title: "Aspose::Words::Drawing::GroupShape class"
linktitle: "GroupShape"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::GroupShape class. تمثل مجموعة من الأشكال في المستند. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.drawing/groupshape/
---
## GroupShape class


يمثل مجموعة من الأشكال في مستند. لمعرفة المزيد، زر مقالة الوثائق [How to Add Group Shape into a Word Document](https://docs.aspose.com/words/cpp/how-to-add-group-shape-into-a-word-document/).

```cpp
class GroupShape : public Aspose::Words::Drawing::ShapeBase
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا لزيارة نهاية [GroupShape](./). |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا لزيارة بداية [GroupShape](./). |
| [AdjustWithEffects](../shapebase/adjustwitheffects/)(System::Drawing::RectangleF) | يضيف إلى المستطيل المصدر قيم مدى التأثير ويعيد المستطيل النهائي. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | ينشئ نسخة مكررة من العقدة. |
| [get_AllowOverlap](../shapebase/get_allowoverlap/)() | يحصل أو يضبط قيمة تحدد ما إذا كان هذا الشكل يمكنه التداخل مع أشكال أخرى. |
| [get_AlternativeText](../shapebase/get_alternativetext/)() | يحدد النص البديل الذي يُعرض بدلاً من الرسم. |
| [get_AnchorLocked](../shapebase/get_anchorlocked/)() | يحدد ما إذا كان مرساة الشكل مقفلة. |
| [get_AspectRatioLocked](../shapebase/get_aspectratiolocked/)() | يحدد ما إذا كان نسبة أبعاد الشكل مقفلة. |
| [get_BehindText](../shapebase/get_behindtext/)() | يحدد ما إذا كان الشكل أسفل أو أعلى النص. |
| [get_Bottom](../shapebase/get_bottom/)() | يحصل على موضع الحافة السفلية للكتلة المحتوية على الشكل. |
| [get_Bounds](../shapebase/get_bounds/)() | يحصل أو يضبط موقع وحجم الكتلة المحتوية على الشكل. |
| [get_BoundsInPoints](../shapebase/get_boundsinpoints/)() | يحصل على موقع وحجم الكتلة المحتوية على الشكل بالنقاط، بالنسبة إلى مرساة الشكل الأعلى. |
| [get_BoundsWithEffects](../shapebase/get_boundswitheffects/)() | يحصل على الامتداد النهائي لهذا الكائن الشكل بعد تطبيق تأثيرات الرسم. القيمة مقاسة بالنقاط. |
| [get_CanHaveImage](../shapebase/get_canhaveimage/)() | يرجع **true** إذا كان نوع الشكل يسمح بوجود صورة. |
| [get_CoordOrigin](../shapebase/get_coordorigin/)() | الإحداثيات في الزاوية العلوية اليسرى للكتلة المحتوية على هذا الشكل. |
| [get_CoordSize](../shapebase/get_coordsize/)() | العرض والارتفاع لمساحة الإحداثيات داخل الكتلة المحتوية على هذا الشكل. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | يحصل على عدد الأطفال المباشرين لهذه العقدة. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | يحدد معرفًا مخصصًا للعقدة. |
| [get_DistanceBottom](../shapebase/get_distancebottom/)() | يرجع أو يضبط المسافة (بالنقاط) بين نص المستند والحافة السفلية للشكل. |
| [get_DistanceLeft](../shapebase/get_distanceleft/)() | يرجع أو يضبط المسافة (بالنقاط) بين نص المستند والحافة اليسرى للشكل. |
| [get_DistanceRight](../shapebase/get_distanceright/)() | يرجع أو يضبط المسافة (بالنقاط) بين نص المستند والحافة اليمنى للشكل. |
| [get_DistanceTop](../shapebase/get_distancetop/)() | يرجع أو يضبط المسافة (بالنقاط) بين نص المستند والحافة العلوية للشكل. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [get_Fill](../shapebase/get_fill/)() | يحصل على تنسيق التعبئة للشكل. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | يحصل على الطفل الأول للعقدة. |
| [get_FlipOrientation](../shapebase/get_fliporientation/)() | يبدل اتجاه الشكل. |
| [get_Font](../shapebase/get_font/)() | يوفر الوصول إلى تنسيق الخط لهذا الكائن. |
| [get_Glow](../shapebase/get_glow/)() | يحصل على تنسيق التوهج للشكل. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | يرجع **true** إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [get_Height](../shapebase/get_height/)() | يحصل أو يضبط ارتفاع الكتلة المحتوية على الشكل. |
| [get_HeightRelative](../shapebase/get_heightrelative/)() | الحصول أو تعيين القيمة التي تمثل نسبة الارتفاع النسبي للشكل. |
| [get_Hidden](../shapebase/get_hidden/)() | الحصول أو تعيين قيمة منطقية تشير إلى ما إذا كان الشكل مرئيًا. |
| [get_HorizontalAlignment](../shapebase/get_horizontalalignment/)() | يحدد كيفية تموضع الشكل أفقيًا. |
| [get_HRef](../shapebase/get_href/)() | الحصول أو تعيين عنوان الارتباط الكامل للشكل. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | يرجع **true** لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [get_IsDecorative](../shapebase/get_isdecorative/)() | الحصول أو تعيين العلامة التي تحدد ما إذا كان الشكل زخرفيًا في المستند. |
| [get_IsDeleteRevision](../shapebase/get_isdeleterevision/)() | يرجع true إذا تم حذف هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsGroup](../shapebase/get_isgroup/)() | إرجاع **true** إذا كان هذا شكل مجموعة. |
| [get_IsHorizontalRule](../shapebase/get_ishorizontalrule/)() | إرجاع **true** إذا كان هذا الشكل قاعدة أفقية. |
| [get_IsImage](../shapebase/get_isimage/)() | إرجاع **true** إذا كان هذا الشكل شكل صورة. |
| [get_IsInline](../shapebase/get_isinline/)() | طريقة سريعة لتحديد ما إذا كان هذا الشكل موضعًا داخل النص. |
| [get_IsInsertRevision](../shapebase/get_isinsertrevision/)() | يرجع true إذا تم إدراج هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsLayoutInCell](../shapebase/get_islayoutincell/)() | الحصول أو تعيين علامة تشير إلى ما إذا كان الشكل معروضًا داخل جدول أو خارجه. |
| [get_IsMoveFromRevision](../shapebase/get_ismovefromrevision/)() | يرجع **true** إذا تم نقل (حذف) هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsMoveToRevision](../shapebase/get_ismovetorevision/)() | يرجع **true** إذا تم نقل (إدراج) هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsSignatureLine](../shapebase/get_issignatureline/)() | يشير إلى أن الشكل هو [SignatureLine](../signatureline/). |
| [get_IsTopLevel](../shapebase/get_istoplevel/)() | إرجاع **true** إذا لم يكن هذا الشكل فرعًا لشكل مجموعة. |
| [get_IsWordArt](../shapebase/get_iswordart/)() | إرجاع **true** إذا كان هذا الشكل كائن WordArt. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | يحصل على الطفل الأخير للعقدة. |
| [get_Left](../shapebase/get_left/)() | الحصول أو تعيين موضع الحافة اليسرى للكتلة المحتوية على الشكل. |
| [get_LeftRelative](../shapebase/get_leftrelative/)() | الحصول أو تعيين القيمة التي تمثل الموضع النسبي الأيسر للشكل بالنسبة المئوية. |
| [get_MarkupLanguage](../shapebase/get_markuplanguage/)() const | الحصول على لغة الترميز المستخدمة لهذا الكائن الرسومي. |
| [get_Name](../shapebase/get_name/)() | الحصول أو تعيين اسم الشكل الاختياري. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | يحصل على العقدة التي تلي هذه العقدة مباشرةً. |
| [get_NodeType](./get_nodetype/)() const override | إرجاع [GroupShape](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | يحصل على الوالد المباشر لهذه العقدة. |
| [get_ParentParagraph](../shapebase/get_parentparagraph/)() | إرجاع الفقرة الأصلية المباشرة. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | يرجع كائن [Range](../../aspose.words/range/) الذي يمثل الجزء من المستند الموجود داخل هذه العقدة. |
| [get_Reflection](../shapebase/get_reflection/)() | الحصول على تنسيق الانعكاس للشكل. |
| [get_RelativeHorizontalPosition](../shapebase/get_relativehorizontalposition/)() | يحدد بالنسبة إلى ماذا يتم تموضع الشكل أفقيًا. |
| [get_RelativeHorizontalSize](../shapebase/get_relativehorizontalsize/)() | الحصول أو تعيين قيمة الحجم النسبي للشكل في الاتجاه الأفقي. |
| [get_RelativeVerticalPosition](../shapebase/get_relativeverticalposition/)() | يحدد بالنسبة إلى ماذا يتم تموضع الشكل عموديًا. |
| [get_RelativeVerticalSize](../shapebase/get_relativeverticalsize/)() | الحصول أو تعيين قيمة الحجم النسبي للشكل في الاتجاه العمودي. |
| [get_Right](../shapebase/get_right/)() | الحصول على موضع الحافة اليمنى للكتلة المحتوية على الشكل. |
| [get_Rotation](../shapebase/get_rotation/)() | يحدد الزاوية (بالدرجات) التي يتم تدوير الشكل بها. القيمة الإيجابية تتطابق مع زاوية الدوران في اتجاه عقارب الساعة. |
| [get_ScreenTip](../shapebase/get_screentip/)() | يحدد النص المعروض عندما يتحرك مؤشر الفأرة فوق الشكل. |
| [get_ShadowFormat](../shapebase/get_shadowformat/)() | يحصل على تنسيق الظل للشكل. |
| [get_ShapeType](../shapebase/get_shapetype/)() | يحصل على نوع الشكل. |
| [get_SizeInPoints](../shapebase/get_sizeinpoints/)() | يحصل على حجم الشكل بالنقاط. |
| [get_SoftEdge](../shapebase/get_softedge/)() | يحصل على تنسيق الحافة الناعمة للشكل. |
| [get_Target](../shapebase/get_target/)() | يحصل أو يضبط إطار الهدف لرابط الشكل. |
| [get_Title](../shapebase/get_title/)() | يحصل أو يضبط العنوان (التسمية) لكائن الشكل الحالي. |
| [get_Top](../shapebase/get_top/)() | يحصل أو يضبط موضع الحافة العلوية للكتلة المحتوية على الشكل. |
| [get_TopRelative](../shapebase/get_toprelative/)() | يحصل أو يضبط القيمة التي تمثل الموضع العلوي النسبي للشكل بالنسبة المئوية. |
| [get_VerticalAlignment](../shapebase/get_verticalalignment/)() | يحدد كيفية تموضع الشكل عمودياً. |
| [get_Width](../shapebase/get_width/)() | يحصل أو يضبط عرض الكتلة المحتوية على الشكل. |
| [get_WidthRelative](../shapebase/get_widthrelative/)() | يحصل أو يضبط القيمة التي تمثل نسبة عرض الشكل النسبي. |
| [get_WrapSide](../shapebase/get_wrapside/)() | يحدد كيفية التفاف النص حول الشكل. |
| [get_WrapType](../shapebase/get_wraptype/)() | يحدد ما إذا كان الشكل مضمناً أو عائمًا. بالنسبة للأشكال العائمة يحدد وضعية التفاف النص حول الشكل. |
| [get_ZOrder](../shapebase/get_zorder/)() | يحدد ترتيب عرض الأشكال المتداخلة. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | يحصل على السلف الأول من النوع المحدد [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | يرجع عقدة الطفل رقم N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | يعيد مجموعة حية من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | يوفر دعمًا لتكرار نمط foreach على العقد الفرعية لهذا العقد. |
| [GetShapeRenderer](../shapebase/getshaperenderer/)() | ينشئ ويعيد كائنًا يمكن استخدامه لتصوير هذا الشكل إلى صورة. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | يحصل على نص هذا العقد وجميع أطفاله. |
| [GetType](./gettype/)() const override |  |
| [GroupShape](./groupshape/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | ينشئ شكل مجموعة جديد. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يعيد فهرس العقدة الفرعية المحددة في مصفوفة العقد الفرعية. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [LocalToParent](../shapebase/localtoparent/)(System::Drawing::PointF) | يحوّل قيمة من مساحة الإحداثيات المحلية إلى مساحة إحداثيات الشكل الأب. |
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
| [set_AllowOverlap](../shapebase/set_allowoverlap/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_AllowOverlap](../shapebase/get_allowoverlap/). |
| [set_AlternativeText](../shapebase/set_alternativetext/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_AlternativeText](../shapebase/get_alternativetext/). |
| [set_AnchorLocked](../shapebase/set_anchorlocked/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_AnchorLocked](../shapebase/get_anchorlocked/). |
| [set_AspectRatioLocked](../shapebase/set_aspectratiolocked/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked](../shapebase/get_aspectratiolocked/). |
| [set_BehindText](../shapebase/set_behindtext/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_BehindText](../shapebase/get_behindtext/). |
| [set_Bounds](../shapebase/set_bounds/)(System::Drawing::RectangleF) | مُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_Bounds](../shapebase/get_bounds/). |
| [set_CoordOrigin](../shapebase/set_coordorigin/)(System::Drawing::Point) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_CoordOrigin](../shapebase/get_coordorigin/). |
| [set_CoordSize](../shapebase/set_coordsize/)(System::Drawing::Size) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_CoordSize](../shapebase/get_coordsize/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DistanceBottom](../shapebase/set_distancebottom/)(double) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_DistanceBottom](../shapebase/get_distancebottom/). |
| [set_DistanceLeft](../shapebase/set_distanceleft/)(double) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_DistanceLeft](../shapebase/get_distanceleft/). |
| [set_DistanceRight](../shapebase/set_distanceright/)(double) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_DistanceRight](../shapebase/get_distanceright/). |
| [set_DistanceTop](../shapebase/set_distancetop/)(double) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_DistanceTop](../shapebase/get_distancetop/). |
| [set_FlipOrientation](../shapebase/set_fliporientation/)(Aspose::Words::Drawing::FlipOrientation) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_FlipOrientation](../shapebase/get_fliporientation/). |
| [set_Height](../shapebase/set_height/)(double) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_Height](../shapebase/get_height/). |
| [set_HeightRelative](../shapebase/set_heightrelative/)(float) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_HeightRelative](../shapebase/get_heightrelative/). |
| [set_Hidden](../shapebase/set_hidden/)(bool) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_Hidden](../shapebase/get_hidden/). |
| [set_HorizontalAlignment](../shapebase/set_horizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment](../shapebase/get_horizontalalignment/). |
| [set_HRef](../shapebase/set_href/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_HRef](../shapebase/get_href/). |
| [set_IsDecorative](../shapebase/set_isdecorative/)(bool) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_IsDecorative](../shapebase/get_isdecorative/). |
| [set_IsLayoutInCell](../shapebase/set_islayoutincell/)(bool) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell](../shapebase/get_islayoutincell/). |
| [set_Left](../shapebase/set_left/)(double) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_Left](../shapebase/get_left/). |
| [set_LeftRelative](../shapebase/set_leftrelative/)(float) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_LeftRelative](../shapebase/get_leftrelative/). |
| [set_Name](../shapebase/set_name/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_Name](../shapebase/get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalPosition](../shapebase/set_relativehorizontalposition/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition](../shapebase/get_relativehorizontalposition/). |
| [set_RelativeHorizontalSize](../shapebase/set_relativehorizontalsize/)(Aspose::Words::Drawing::RelativeHorizontalSize) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize](../shapebase/get_relativehorizontalsize/). |
| [set_RelativeVerticalPosition](../shapebase/set_relativeverticalposition/)(Aspose::Words::Drawing::RelativeVerticalPosition) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition](../shapebase/get_relativeverticalposition/). |
| [set_RelativeVerticalSize](../shapebase/set_relativeverticalsize/)(Aspose::Words::Drawing::RelativeVerticalSize) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize](../shapebase/get_relativeverticalsize/). |
| [set_Rotation](../shapebase/set_rotation/)(double) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_Rotation](../shapebase/get_rotation/). |
| [set_ScreenTip](../shapebase/set_screentip/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_ScreenTip](../shapebase/get_screentip/). |
| [set_Target](../shapebase/set_target/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_Target](../shapebase/get_target/). |
| [set_Title](../shapebase/set_title/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Drawing::ShapeBase::get_Title](../shapebase/get_title/). |
| [set_Top](../shapebase/set_top/)(double) | دالة تعيين لـ [Aspose::Words::Drawing::ShapeBase::get_Top](../shapebase/get_top/). |
| [set_TopRelative](../shapebase/set_toprelative/)(float) | دالة تعيين لـ [Aspose::Words::Drawing::ShapeBase::get_TopRelative](../shapebase/get_toprelative/). |
| [set_VerticalAlignment](../shapebase/set_verticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | دالة تعيين لـ [Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment](../shapebase/get_verticalalignment/). |
| [set_Width](../shapebase/set_width/)(double) | دالة تعيين لـ [Aspose::Words::Drawing::ShapeBase::get_Width](../shapebase/get_width/). |
| [set_WidthRelative](../shapebase/set_widthrelative/)(float) | دالة تعيين لـ [Aspose::Words::Drawing::ShapeBase::get_WidthRelative](../shapebase/get_widthrelative/). |
| [set_WrapSide](../shapebase/set_wrapside/)(Aspose::Words::Drawing::WrapSide) | دالة تعيين لـ [Aspose::Words::Drawing::ShapeBase::get_WrapSide](../shapebase/get_wrapside/). |
| [set_WrapType](../shapebase/set_wraptype/)(Aspose::Words::Drawing::WrapType) | دالة تعيين لـ [Aspose::Words::Drawing::ShapeBase::get_WrapType](../shapebase/get_wraptype/). |
| [set_ZOrder](../shapebase/set_zorder/)(int32_t) | دالة تعيين لـ [Aspose::Words::Drawing::ShapeBase::get_ZOrder](../shapebase/get_zorder/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | يصدّر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يصدّر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| static [Type](./type/)() |  |
## ملاحظات


تُعد [GroupShape](./) عقدة مركبة ويمكن أن تحتوي على عقد [Shape](../shape/) و[GroupShape](./) كعناصر فرعية.

كل [GroupShape](./) يعرّف نظام إحداثيات جديد لأشكاله الفرعية. يتم تعريف نظام الإحداثيات باستخدام خصائص [CoordSize](../shapebase/get_coordsize/) و[CoordOrigin](../shapebase/get_coordorigin/).

## انظر أيضًا

* Class [ShapeBase](../shapebase/)
* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
