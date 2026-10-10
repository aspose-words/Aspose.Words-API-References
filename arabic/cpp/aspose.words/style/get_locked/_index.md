---
title: "Aspose::Words::Style::get_Locked طريقة"
linktitle: "get_Locked"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Style::get_Locked طريقة. يحدد ما إذا كان هذا النمط مقفولًا في C++."
type: docs
weight: 13500
url: /ar/cpp/aspose.words/style/get_locked/
---
## Style::get_Locked method


يحدد ما إذا كان هذا النمط مقفلًا.

```cpp
bool Aspose::Words::Style::get_Locked() const
```


## أمثلة



يوضح كيفية قفل النمط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> styleHeading1 = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Heading1);
if (!styleHeading1->get_Locked())
{
    styleHeading1->set_Locked(true);
}

doc->Save(get_ArtifactsDir() + u"Styles.LockStyle.docx");
```

## انظر أيضًا

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
