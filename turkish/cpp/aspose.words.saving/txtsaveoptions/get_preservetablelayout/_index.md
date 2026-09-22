---
title: "Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout yöntemi"
linktitle: "get_PreserveTableLayout"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout yöntemi. Programın düz metin formatında kaydederken tabloların düzenini korumaya çalışıp çalışmayacağını belirtir. Varsayılan değer C++'ta false'tur."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.saving/txtsaveoptions/get_preservetablelayout/
---
## TxtSaveOptions::get_PreserveTableLayout method


Programın düz metin formatında kaydederken tabloların düzenini korumaya çalışıp çalışmayacağını belirtir. Varsayılan değer **false**'dır.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout() const
```


## Örnekler



Tabloların düzenini düz metne dönüştürürken nasıl koruyacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1");
builder->InsertCell();
builder->Write(u"Row 1, cell 2");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, cell 1");
builder->InsertCell();
builder->Write(u"Row 2, cell 2");
builder->EndTable();

// Bir "TxtSaveOptions" nesnesi oluşturun, bunu belgenin "Save" yöntemine aktarabiliriz
// belgeyi düz metne kaydetme şeklini değiştirmek için.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// "PreserveTableLayout" özelliğini "true" olarak ayarlayın, içeriğe boşluk doldurması uygulamak için
// çıktı düz metin belgesinde tablo düzeninin mümkün olduğunca çok kısmını korumak için.
// "PreserveTableLayout" özelliğini "false" olarak ayarlayın, tüm tabloların içeriğini kaydetmek için
// her satır için sadece yeni bir satırla, kesintisiz bir metin gövdesi olarak.
txtSaveOptions->set_PreserveTableLayout(preserveTableLayout);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.PreserveTableLayout.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.PreserveTableLayout.txt");

if (preserveTableLayout)
{
    ASSERT_EQ(System::String(u"Row 1, cell 1                                            Row 1, cell 2\r\n") + u"Row 2, cell 1                                            Row 2, cell 2\r\n\r\n", docText);
}
else
{
    ASSERT_EQ(System::String(u"Row 1, cell 1\r") + u"Row 1, cell 2\r" + u"Row 2, cell 1\r" + u"Row 2, cell 2\r\r\n", docText);
}
```

## Ayrıca Bakınız

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
