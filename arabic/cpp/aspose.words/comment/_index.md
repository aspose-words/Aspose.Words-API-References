---
title: "Aspose::Words::Comment class"
linktitle: "Comment"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Comment class. يمثل حاوية لنص التعليق. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words/comment/
---
## Comment class


يمثل حاوية لنص التعليق. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Working with Comments](https://docs.aspose.com/words/cpp/working-with-comments/).

```cpp
class Comment : public Aspose::Words::InlineStory,
                public Aspose::Words::INodeWithAnnotationId,
                public Aspose::Words::Revisions::IMoveTrackableNode
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا لزيارة نهاية التعليق. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا لزيارة بداية التعليق. |
| [AddReply](./addreply/)(const System::String\&, const System::String\&, System::DateTime, const System::String\&) | يضيف ردًا على هذا التعليق. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | ينشئ نسخة مكررة من العقدة. |
| [Comment](./comment/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | ينشئ نسخة جديدة من الفئة [Comment](./). |
| [Comment](./comment/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&, const System::String\&, System::DateTime) | ينشئ نسخة جديدة من الفئة [Comment](./). |
| [EnsureMinimum](../inlinestory/ensureminimum/)() | إذا لم يكن العنصر الفرعي الأخير فقرة، ينشئ ويضيف فقرة فارغة واحدة. |
| [get_Ancestor](./get_ancestor/)() | يرجع كائن [Comment](./) الأب. يرجع **null** للتعليقات ذات المستوى الأعلى. |
| [get_Author](./get_author/)() const | يرجع أو يعيّن اسم المؤلف للتعليق. |
| [get_Count](../compositenode/get_count/)() | يحصل على عدد الأطفال المباشرين لهذه العقدة. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | يحدد معرفًا مخصصًا للعقدة. |
| [get_DateTime](./get_datetime/)() const | يحصل على التاريخ والوقت الذي تم فيه إنشاء التعليق. |
| [get_DateTimeUtc](./get_datetimeutc/)() | يحصل على تاريخ ووقت UTC الذي تم فيه إنشاء التعليق. |
| virtual [get_Document](../node/get_document/)() const | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [get_Done](./get_done/)() const | يحصل أو يعيّن علامة تشير إلى أن التعليق تم وضع علامة done عليه. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | يحصل على الطفل الأول للعقدة. |
| [get_FirstParagraph](../inlinestory/get_firstparagraph/)() override | يحصل على الفقرة الأولى في القصة. |
| [get_Font](../inlinestory/get_font/)() | يوفر الوصول إلى تنسيق الخط لحرف المرجع لهذا الكائن. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | يرجع **true** إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [get_Id](./get_id/)() const | يحصل أو يعيّن معرف التعليق. |
| [get_Initial](./get_initial/)() const | يرجع أو يعيّن الأحرف الأولى للمستخدم المرتبط بتعليق محدد. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | يرجع **true** لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [get_IsDeleteRevision](../inlinestory/get_isdeleterevision/)() | يرجع true إذا تم حذف هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsInsertRevision](../inlinestory/get_isinsertrevision/)() | يرجع true إذا تم إدراج هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsMoveFromRevision](../inlinestory/get_ismovefromrevision/)() | يرجع **true** إذا تم نقل (حذف) هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsMoveToRevision](../inlinestory/get_ismovetorevision/)() | يرجع **true** إذا تم نقل (إدراج) هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_LastChild](../compositenode/get_lastchild/)() const | يحصل على الطفل الأخير للعقدة. |
| [get_LastParagraph](../inlinestory/get_lastparagraph/)() override | يحصل على الفقرة الأخيرة في القصة. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | يحصل على العقدة التي تلي هذه العقدة مباشرةً. |
| [get_NodeType](./get_nodetype/)() const override | يرجع [Comment](../nodetype/). |
| [get_Paragraphs](../inlinestory/get_paragraphs/)() override | يحصل على مجموعة من الفقرات التي هي أطفال مباشرون للقصة. |
| [get_ParentId](./get_parentid/)() const | يحصل على معرف التعليق الأب. القيمة **%-1** تعني أن التعليق ليس له أب. |
| [get_ParentNode](../node/get_parentnode/)() | يحصل على الوالد المباشر لهذه العقدة. |
| [get_ParentParagraph](../inlinestory/get_parentparagraph/)() | يسترجع العنصر الأب [Paragraph](../paragraph/) لهذه العقدة. |
| [get_PreviousSibling](../node/get_previoussibling/)() | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | يعيد كائن [Range](../range/) الذي يمثل الجزء من المستند الموجود داخل هذه العقدة. |
| [get_Replies](./get_replies/)() | يعيد مجموعة من كائنات [Comment](./) التي هي أبناء فوريون للتعليق المحدد. |
| [get_StoryType](./get_storytype/)() override | يعيد [Comments](../storytype/). |
| [get_Tables](../inlinestory/get_tables/)() override | يحصل على مجموعة من الجداول التي هي أطفال مباشرون للقصة. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | يحصل على السلف الأول من النوع المحدد [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | يرجع عقدة الطفل رقم N التي تطابق النوع المحدد. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | يعيد مجموعة حية من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../compositenode/getenumerator/)() override | يوفر دعمًا لتكرار نمط foreach على العقد الفرعية لهذا العقد. |
| [GetText](../compositenode/gettext/)() override | يحصل على نص هذا العقد وجميع أطفاله. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يعيد فهرس العقدة الفرعية المحددة في مصفوفة العقد الفرعية. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على العقدة التالية وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | طريقة مساعدة تقوم بتحويل قيمة تعداد نوع العقدة إلى سلسلة صديقة للمستخدم. |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب. |
| [Remove](../node/remove/)() | يزيل نفسه من العنصر الأب. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | يزيل جميع العقد الفرعية للعقدة الحالية. |
| [RemoveAllReplies](./removeallreplies/)() | يزيل جميع الردود على هذا التعليق. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveReply](./removereply/)(const System::SharedPtr\<Aspose::Words::Comment\>\&) | يزيل الرد المحدد على هذا التعليق. |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | يزيل جميع العقد التابعة لـ [SmartTag](../../aspose.words.markup/smarttag/) للعقدة الحالية. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | يختار قائمة من العقد التي تطابق تعبير XPath. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | يختار أول [Node](../node/) يطابق تعبير XPath. |
| [set_Author](./set_author/)(const System::String\&) | دالة تعيين لـ [Aspose::Words::Comment::get_Author](./get_author/). |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | دالة الضبط لـ [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_DateTime](./set_datetime/)(System::DateTime) | يحصل على التاريخ والوقت الذي تم فيه إنشاء التعليق. |
| [set_Done](./set_done/)(bool) | دالة تعيين لـ [Aspose::Words::Comment::get_Done](./get_done/). |
| [set_Id](./set_id/)(int32_t) | دالة تعيين لـ [Aspose::Words::Comment::get_Id](./get_id/). |
| [set_Initial](./set_initial/)(const System::String\&) | دالة تعيين لـ [Aspose::Words::Comment::get_Initial](./get_initial/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ParentId](./set_parentid/)(int32_t) | يضبط معرف التعليق الأب. القيمة **%-1** تعني أن التعليق ليس له أب. |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SetText](./settext/)(const System::String\&) | هذه طريقة مريحة تسمح بتعيين نص التعليق بسهولة. |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | يصدّر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يصدّر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| static [Type](./type/)() |  |
## ملاحظات


التعليق هو توضيح يتم تثبيته على منطقة من النص أو على موضع في النص. يمكن للتعليق أن يحتوي على كمية عشوائية من المحتوى على مستوى الكتلة.

إذا ظهر كائن [Comment](./) بمفرده، يتم تثبيت التعليق على موضع كائن [Comment](./).

لتثبيت تعليق على منطقة من النص يلزم ثلاثة كائنات: [Comment](./)، [CommentRangeStart](../commentrangestart/) و[CommentRangeEnd](../commentrangeend/). يجب أن تشترك جميع الكائنات الثلاثة في نفس قيمة [Id](./get_id/).

[Comment](./) is an inline-level node and can only be a child of [Paragraph](../paragraph/).

[Comment](./) can contain [Paragraph](../paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.

## أمثلة



يوضح كيفية إضافة تعليق إلى مستند، ثم الرد عليه.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

// ضع التعليق عند عقدة في جسم المستند.
// سيظهر هذا التعليق في موقع الفقرة الخاصة به،
// خارج الهامش الأيمن للصفحة، ومع خط منقط يربطه بفقرتها.
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// أضف ردًا، سيظهر تحت التعليق الأب.
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");

// التعليقات والردود كلاهما عقد من نوع Comment.
ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Comment, true)->get_Count());

// التعليقات التي لا ترد على تعليقات أخرى هي "مستوى أعلى". ليس لها تعليقات سلفية.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_Ancestor()));

// الردود لها تعليق سلفي من المستوى الأعلى.
ASPOSE_ASSERT_EQ(comment, comment->get_Replies()->idx_get(0)->get_Ancestor());

doc->Save(get_ArtifactsDir() + u"Comment.AddCommentWithReply.docx");
```


يعرض كيفية إضافة تعليق إلى فقرة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// في Microsoft Word، يمكننا النقر بزر الماوس الأيمن على هذا التعليق في جسم المستند لتعديله، أو الرد عليه.
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## انظر أيضًا

* Class [InlineStory](../inlinestory/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
