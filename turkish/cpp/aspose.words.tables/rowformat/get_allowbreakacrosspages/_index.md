---
title: "Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages method"
linktitle: "get_AllowBreakAcrossPages"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages method. C++'ta bir tablo satırındaki metnin sayfa sonu boyunca bölünmesine izin veriliyorsa doğru."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.tables/rowformat/get_allowbreakacrosspages/
---
## RowFormat::get_AllowBreakAcrossPages method


Bir tablo satırındaki metnin sayfa sonu boyunca bölünmesine izin veriliyorsa doğru.

```cpp
bool Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages()
```


## Örnekler



Bir tablodaki her satır için satırların sayfalar arasında bölünmesini nasıl devre dışı bırakacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table spanning two pages.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// "AllowBreakAcrossPages" özelliğini "false" olarak ayarlayın, satırı korumak için
// tablo iki sayfaya yayıldığında satırı tek parça tutar, bu satır boyunca bölünür.
// Satır bir sayfaya sığmayacak kadar büyükse, Microsoft Word onu bir sonraki sayfaya itecektir.
// "AllowBreakAcrossPages" özelliğini "true" olarak ayarlayın, satırın iki sayfa boyunca bölünmesine izin vermek için.
for (auto&& row : System::IterateOver<Aspose::Words::Tables::Row>(table))
{
    row->get_RowFormat()->set_AllowBreakAcrossPages(allowBreakAcrossPages);
}

doc->Save(get_ArtifactsDir() + u"Table.AllowBreakAcrossPages.docx");
```

## Ayrıca Bakınız

* Class [RowFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
