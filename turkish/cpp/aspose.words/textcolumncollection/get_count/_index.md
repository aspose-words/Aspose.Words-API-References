---
title: "Aspose::Words::TextColumnCollection::get_Count yöntemi"
linktitle: "get_Count"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TextColumnCollection::get_Count yöntemi. C++'ta bir belgenin bölümündeki sütun sayısını alır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/textcolumncollection/get_count/
---
## TextColumnCollection::get_Count method


Belgenin bir bölümündeki sütun sayısını alır.

```cpp
int32_t Aspose::Words::TextColumnCollection::get_Count()
```


## Örnekler



Bir bölümde birden fazla eşit aralıklı sütun oluşturmayı gösterir.
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

## Ayrıca Bakınız

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
