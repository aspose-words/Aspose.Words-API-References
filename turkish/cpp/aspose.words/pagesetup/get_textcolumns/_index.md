---
title: "Aspose::Words::PageSetup::get_TextColumns yöntemi"
linktitle: "get_TextColumns"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_TextColumns yöntemi. C++'ta metin sütunları kümesini temsil eden bir koleksiyon döndürür."
type: docs
weight: 44000
url: /tr/cpp/aspose.words/pagesetup/get_textcolumns/
---
## PageSetup::get_TextColumns method


Metin sütunlarını temsil eden bir koleksiyon döndürür.

```cpp
System::SharedPtr<Aspose::Words::TextColumnCollection> Aspose::Words::PageSetup::get_TextColumns()
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

* Class [TextColumnCollection](../../textcolumncollection/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
