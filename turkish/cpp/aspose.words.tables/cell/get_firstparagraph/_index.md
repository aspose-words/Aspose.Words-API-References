---
title: "Aspose::Words::Tables::Cell::get_FirstParagraph yöntemi"
linktitle: "get_FirstParagraph"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Cell::get_FirstParagraph yöntemi. C++'de doğrudan alt öğeler arasında ilk paragrafı alır."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.tables/cell/get_firstparagraph/
---
## Cell::get_FirstParagraph method


Doğrudan çocuklar arasında ilk paragrafı alır.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Tables::Cell::get_FirstParagraph()
```


## Örnekler



Bir belge oluşturucu kullanarak iç içe tablo oluşturmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Dış tabloyu oluştur.
System::SharedPtr<Aspose::Words::Tables::Cell> cell = builder->InsertCell();
builder->Writeln(u"Outer Table Cell 1");
builder->InsertCell();
builder->Writeln(u"Outer Table Cell 2");
builder->EndTable();

// Dış tablonun ilk hücresine geçin, ardından hücrenin içinde başka bir tablo oluşturun.
builder->MoveTo(cell->get_FirstParagraph());
builder->InsertCell();
builder->Writeln(u"Inner Table Cell 1");
builder->InsertCell();
builder->Writeln(u"Inner Table Cell 2");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertNestedTable.docx");
```

## Ayrıca Bakınız

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
