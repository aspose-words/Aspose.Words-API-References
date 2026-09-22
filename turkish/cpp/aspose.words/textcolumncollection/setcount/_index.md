---
title: "Aspose::Words::TextColumnCollection::SetCount metodu"
linktitle: "SetCount"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TextColumnCollection::SetCount metodu. C++'da metni belirtilen sayıdaki metin sütununa düzenler."
type: docs
weight: 13000
url: /tr/cpp/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection::SetCount method


Metni belirtilen sayıda metin sütununa düzenler.

```cpp
void Aspose::Words::TextColumnCollection::SetCount(int32_t newCount)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| newCount | int32_t | Metnin düzenleneceği sütun sayısı. |
## Açıklamalar


[EvenlySpaced](../get_evenlyspaced/) **false** olduğunda ve sütun sayısını artırdığınızda, yeni [TextColumn](../../textcolumn/) nesneleri sıfır genişlik ve boşlukla oluşturulur. Yeni sütunlar için genişlik ve boşluğu ayarlamanız gerekir.

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
