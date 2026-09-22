---
title: "Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels method"
linktitle: "get_SimplifyListLabels"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels yöntemi. Programın, karmaşık etiket biçimlendirmesi düz metinle yeterince temsil edilemediğinde liste etiketlerini basitleştirip basitleştirmeyeceğini belirtir. true olarak ayarlanırsa, numaralı liste etiketleri basit sayısal formatta ve madde işaretli liste etiketleri basit ASCII karakterleri olarak yazılır. Varsayılan değer C++'ta false'tur."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.saving/txtsaveoptions/get_simplifylistlabels/
---
## TxtSaveOptions::get_SimplifyListLabels method


Programın, karmaşık etiket biçimlendirmesinin düz metinle yeterince temsil edilemediği durumlarda liste etiketlerini basitleştirip basitleştirmeyeceğini belirtir. **true** olarak ayarlanırsa, numaralı liste etiketleri basit sayısal formatta, madde işaretli liste etiketleri ise basit ASCII karakterleriyle yazılır. Varsayılan değer **false**'dır.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels() const
```


## Örnekler



Bir belgeyi düz metne kaydederken listelerin görünümünü nasıl değiştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Beş girinti seviyesine sahip bir madde işaretli liste oluşturun.
builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Item 1");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 2");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 3");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 4");
builder->get_ListFormat()->ListIndent();
builder->Write(u"Item 5");

// Bir "TxtSaveOptions" nesnesi oluşturun, bunu belgenin "Save" yöntemine aktarabiliriz
// belgeyi düz metne kaydetme şeklini değiştirmek için.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Bazı listeyi dönüştürmek için "SimplifyListLabels" özelliğini "true" olarak ayarlayın
// sembolleri '*', 'o', '+', '>', vb. gibi daha basit ASCII karakterlerine dönüştürür.
// "SimplifyListLabels" özelliğini "false" olarak ayarlayarak mümkün olduğunca çok orijinal liste sembolünü koruyun.
txtSaveOptions->set_SimplifyListLabels(simplifyListLabels);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.SimplifyListLabels.txt");

System::String newLine = System::Environment::get_NewLine();
if (simplifyListLabels)
{
    ASSERT_EQ(System::String::Format(u"* Item 1{0}", newLine) + System::String::Format(u"  > Item 2{0}", newLine) + System::String::Format(u"    + Item 3{0}", newLine) + System::String::Format(u"      - Item 4{0}", newLine) + System::String::Format(u"        o Item 5{0}", newLine), docText);
}
else
{
    ASSERT_EQ(System::String::Format(u"· Item 1{0}", newLine) + System::String::Format(u"o Item 2{0}", newLine) + System::String::Format(u"§ Item 3{0}", newLine) + System::String::Format(u"· Item 4{0}", newLine) + System::String::Format(u"o Item 5{0}", newLine), docText);
}
```

## Ayrıca Bakınız

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
