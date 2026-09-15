---
title: "Aspose::Words::PageSetup::get_TextColumns طريقة"
linktitle: "get_TextColumns"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::PageSetup::get_TextColumns طريقة. تُرجع مجموعة تمثل مجموعة أعمدة النص في C++."
type: docs
weight: 44000
url: /ar/cpp/aspose.words/pagesetup/get_textcolumns/
---
## PageSetup::get_TextColumns method


إرجاع مجموعة تمثل مجموعة أعمدة النص.

```cpp
System::SharedPtr<Aspose::Words::TextColumnCollection> Aspose::Words::PageSetup::get_TextColumns()
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

* Class [TextColumnCollection](../../textcolumncollection/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
