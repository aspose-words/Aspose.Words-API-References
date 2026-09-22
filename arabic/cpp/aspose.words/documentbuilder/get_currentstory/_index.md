---
title: "Aspose::Words::DocumentBuilder::get_CurrentStory method"
linktitle: "get_CurrentStory"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentBuilder::get_CurrentStory method. يحصل على القصة التي تم اختيارها حاليًا في هذا DocumentBuilder في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words/documentbuilder/get_currentstory/
---
## DocumentBuilder::get_CurrentStory method


يحصل على القصة التي تم اختيارها حاليًا في هذا [DocumentBuilder](../).

```cpp
System::SharedPtr<Aspose::Words::Story> Aspose::Words::DocumentBuilder::get_CurrentStory()
```


## أمثلة



يعرض كيفية العمل مع القصة الحالية لمُنشئ المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Story هي نوع من العقد التي تحتوي على عقد Paragraph فرعية، مثل Body.
ASPOSE_ASSERT_EQ(builder->get_CurrentStory(), doc->get_FirstSection()->get_Body());
ASPOSE_ASSERT_EQ(builder->get_CurrentStory(), builder->get_CurrentParagraph()->get_ParentNode());
ASSERT_EQ(Aspose::Words::StoryType::MainText, builder->get_CurrentStory()->get_StoryType());

builder->get_CurrentStory()->AppendParagraph(u"Text added to current Story.");

// Story يمكنه أيضًا احتواء جداول.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1");
builder->InsertCell();
builder->Write(u"Row 1, cell 2");
builder->EndTable();

ASSERT_TRUE(builder->get_CurrentStory()->get_Tables()->Contains(table));
```

## انظر أيضًا

* Class [Story](../../story/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
