---
title: "طريقة Aspose::Words::Lists::ListLevel::RemoveTabStop"
linktitle: "RemoveTabStop"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Lists::ListLevel::RemoveTabStop. يزيل علامة التبويب من مستوى القائمة في C++."
type: docs
weight: 22500
url: /ar/cpp/aspose.words.lists/listlevel/removetabstop/
---
## ListLevel::RemoveTabStop method


يزيل علامة التبويب من المستوى من القائمة.

```cpp
void Aspose::Words::Lists::ListLevel::RemoveTabStop()
```


## أمثلة



يظهر كيفية مسح علامة تبويب مستوى القائمة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إنشاء قائمة بالتنسيق الافتراضي
builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");

// احصل على مستوى القائمة وأزل علامة التبويب الخاصة به
System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = builder->get_ListFormat()->get_ListLevel();
listLevel->RemoveTabStop();

doc->Save(get_ArtifactsDir() + u"Paragraph.RemoveTabStopFromListLevel.docx");
```

## انظر أيضًا

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
