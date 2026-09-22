---
title: "Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag طريقة"
linktitle: "MoveToStructuredDocumentTag"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag طريقة. ينقل المؤشر إلى علامة المستند المهيكلة في C++."
type: docs
weight: 61000
url: /ar/cpp/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## DocumentBuilder::MoveToStructuredDocumentTag(const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\&, int32_t) method


ينقل المؤشر إلى علامة المستند المنظم.

```cpp
void Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag(const System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> &structuredDocumentTag, int32_t characterIndex)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| structuredDocumentTag | const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\& | علامة المستند المهيكلة التي سيتم الانتقال إليها. |
| characterIndex | int32_t | فهرس الحرف داخل علامة المستند المهيكلة. القيمة السالبة تسمح لك بتحديد موقع من نهاية علامة المستند المهيكلة. استخدم -1 للانتقال إلى نهاية علامة المستند المهيكلة. إذا كانت علامة المستند المهيكلة على مستوى الكتلة، وتريد نقل المؤشر إلى نهاية الفقرة الأخيرة لها، حدد -2. |

## أمثلة



يظهر كيفية نقل مؤشر [DocumentBuilder](../) داخل علامة المستند المهيكلة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// هناك عدة طرق لتحريك المؤشر:
// 1 -  الانتقال إلى الحرف الأول لعلامة المستند المهيكلة حسب الفهرس.
builder->MoveToStructuredDocumentTag(1, 1);

// 2 -  الانتقال إلى الحرف الأول لعلامة المستند المهيكلة حسب الكائن.
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 2, true));
builder->MoveToStructuredDocumentTag(tag, 1);
builder->Write(u" New text.");

ASSERT_EQ(u"R New text.ichText", tag->GetText().Trim());

// 3 -  الانتقال إلى نهاية علامة المستند المهيكلة الثانية.
builder->MoveToStructuredDocumentTag(1, -1);
ASSERT_TRUE(builder->get_IsAtEndOfStructuredDocumentTag());

// احصل على علامة المستند المهيكلة المحددة حاليًا.
builder->get_CurrentStructuredDocumentTag()->set_Color(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Document.MoveToStructuredDocumentTag.docx");
```

## انظر أيضًا

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::MoveToStructuredDocumentTag(int32_t, int32_t) method


ينقل المؤشر إلى علامة مستند منظم في القسم الحالي.

```cpp
void Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag(int32_t structuredDocumentTagIndex, int32_t characterIndex)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| structuredDocumentTagIndex | int32_t | فهرس علامة المستند المهيكلة التي تريد الانتقال إليها. |
| characterIndex | int32_t | فهرس الحرف داخل علامة المستند المهيكلة. القيمة السالبة تسمح لك بتحديد موقع من نهاية علامة المستند المهيكلة. استخدم -1 للانتقال إلى نهاية علامة المستند المهيكلة. إذا كانت علامة المستند المهيكلة على مستوى الكتلة، وتريد نقل المؤشر إلى نهاية الفقرة الأخيرة لها، حدد -2. |
## ملاحظات


يتم التنقل داخل القصة الحالية للقسم الحالي. أي إذا قمت بنقل المؤشر إلى رأس القسم الأول الأساسي، فإن *structuredDocumentTagIndex* يحدد فهرس علامة المستند المهيكلة داخل ذلك الرأس من ذلك القسم.

عندما يكون *structuredDocumentTagIndex* أكبر من أو يساوي 0، فإنه يحدد فهرسًا من بداية القسم حيث 0 هو أول علامة مستند مهيكلة. عندما يكون *structuredDocumentTagIndex* أقل من 0، فإنه يحدد فهرسًا من نهاية القسم حيث -1 هو آخر علامة مستند مهيكلة.

## أمثلة



يظهر كيفية نقل مؤشر [DocumentBuilder](../) داخل علامة المستند المهيكلة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// هناك عدة طرق لتحريك المؤشر:
// 1 -  الانتقال إلى الحرف الأول لعلامة المستند المهيكلة حسب الفهرس.
builder->MoveToStructuredDocumentTag(1, 1);

// 2 -  الانتقال إلى الحرف الأول لعلامة المستند المهيكلة حسب الكائن.
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 2, true));
builder->MoveToStructuredDocumentTag(tag, 1);
builder->Write(u" New text.");

ASSERT_EQ(u"R New text.ichText", tag->GetText().Trim());

// 3 -  الانتقال إلى نهاية علامة المستند المهيكلة الثانية.
builder->MoveToStructuredDocumentTag(1, -1);
ASSERT_TRUE(builder->get_IsAtEndOfStructuredDocumentTag());

// احصل على علامة المستند المهيكلة المحددة حاليًا.
builder->get_CurrentStructuredDocumentTag()->set_Color(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Document.MoveToStructuredDocumentTag.docx");
```

## انظر أيضًا

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
