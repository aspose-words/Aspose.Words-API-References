---
title: "طريقة Aspose::Words::TextColumnCollection::get_Count"
linktitle: "get_Count"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::TextColumnCollection::get_Count. يحصل على عدد الأعمدة في قسم المستند في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/textcolumncollection/get_count/
---
## TextColumnCollection::get_Count method


يحصل على عدد الأعمدة في قسم المستند.

```cpp
int32_t Aspose::Words::TextColumnCollection::get_Count()
```


## أمثلة



يوضح كيفية إنشاء أعمدة متعددة موزعة بالتساوي في قسم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_Spacing(100);
columns->SetCount(2);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ColumnsSameWidth.docx");
```

## انظر أيضًا

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
