---
title: "Aspose::Words::TextColumnCollection::get_Spacing metodu"
linktitle: "get_Spacing"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TextColumnCollection::get_Spacing metodu. Sütunlar eşit aralıklı olduğunda, C++'da her sütun arasındaki boşluk miktarını nokta cinsinden alır veya ayarlar."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/textcolumncollection/get_spacing/
---
## TextColumnCollection::get_Spacing method


Sütunlar eşit aralıklı olduğunda, her sütun arasındaki boşluk miktarını nokta cinsinden alır veya ayarlar.

```cpp
double Aspose::Words::TextColumnCollection::get_Spacing()
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
