---
title: "Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag method"
linktitle: "get_CurrentStructuredDocumentTag"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag method. يحصل على علامة المستند الهيكلية التي تم اختيارها حاليًا في هذا DocumentBuilder في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words/documentbuilder/get_currentstructureddocumenttag/
---
## DocumentBuilder::get_CurrentStructuredDocumentTag method


يحصل على علامة المستند الهيكلية التي تم اختيارها حاليًا في هذا [DocumentBuilder](../).

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag()
```


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
