---
title: "Aspose::Words::TextColumnCollection::get_Spacing طريقة"
linktitle: "get_Spacing"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::TextColumnCollection::get_Spacing طريقة. عندما تكون الأعمدة متباعدة بالتساوي، يحصل على أو يضبط مقدار المسافة بين كل عمود بالنقاط في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words/textcolumncollection/get_spacing/
---
## TextColumnCollection::get_Spacing method


عند توزيع الأعمدة بالتساوي، يحصل أو يحدد مقدار المسافة بين كل عمود بالنقاط.

```cpp
double Aspose::Words::TextColumnCollection::get_Spacing()
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
