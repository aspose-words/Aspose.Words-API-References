---
title: "Aspose::Words::TextColumnCollection::get_Width yöntemi"
linktitle: "get_Width"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TextColumnCollection::get_Width yöntemi. Sütunlar eşit aralıkta olduğunda, C++'ta sütunların genişliğini alır."
type: docs
weight: 6000
url: /tr/cpp/aspose.words/textcolumncollection/get_width/
---
## TextColumnCollection::get_Width method


Sütunlar eşit aralıklı olduğunda, sütunların genişliğini alır.

```cpp
double Aspose::Words::TextColumnCollection::get_Width()
```

## Açıklamalar


Yalnızca [EvenlySpaced](../get_evenlyspaced/) **true** olarak ayarlandığında etki gösterir.

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
