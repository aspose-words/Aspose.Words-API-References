---
title: "Aspose::Words::TextColumnCollection sınıfı"
linktitle: "TextColumnCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TextColumnCollection sınıfı. Bir belge bölümündeki tüm metin sütunlarını temsil eden TextColumn nesnelerinin koleksiyonu. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 71000
url: /tr/cpp/aspose.words/textcolumncollection/
---
## TextColumnCollection class


Bir belge bölümündeki tüm metin sütunlarını temsil eden [TextColumn](../textcolumn/) nesnelerinin koleksiyonu. Daha fazla bilgi edinmek için [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/) belge makalesini ziyaret edin.

```cpp
class TextColumnCollection : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Count](./get_count/)() | Belgenin bir bölümündeki sütun sayısını alır. |
| [get_EvenlySpaced](./get_evenlyspaced/)() | Metin sütunları eşit genişlikte ve eşit aralıklıysa True. |
| [get_LineBetween](./get_linebetween/)() | **true** olduğunda, sütunlar arasında dikey bir çizgi ekler. |
| [get_Spacing](./get_spacing/)() | Sütunlar eşit aralıklı olduğunda, her sütun arasındaki boşluk miktarını nokta cinsinden alır veya ayarlar. |
| [get_Width](./get_width/)() | Sütunlar eşit aralıklı olduğunda, sütunların genişliğini alır. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Belirtilen indeksteki bir metin sütununu döndürür. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_EvenlySpaced](./set_evenlyspaced/)(bool) | [Aspose::Words::TextColumnCollection::get_EvenlySpaced](./get_evenlyspaced/) için ayarlayıcı. |
| [set_LineBetween](./set_linebetween/)(bool) | [Aspose::Words::TextColumnCollection::get_LineBetween](./get_linebetween/) için ayarlayıcı. |
| [set_Spacing](./set_spacing/)(double) | [Aspose::Words::TextColumnCollection::get_Spacing](./get_spacing/) için ayarlayıcı. |
| [SetCount](./setcount/)(int32_t) | Metni belirtilen sayıda metin sütununa düzenler. |
| static [Type](./type/)() |  |
## Açıklamalar


Metin sütunlarının sayısını ayarlamak için [SetCount()](./setcount/) kullanın.

Tüm sütunların eşit genişlikte ve eşit aralıklı olmasını sağlamak için [EvenlySpaced](./get_evenlyspaced/) özelliğini **true** olarak ayarlayın ve sütunlar arasındaki boşluk miktarını [Spacing](./get_spacing/) içinde belirtin. MS Word otomatik olarak sütun genişliklerini hesaplayacaktır.

[EvenlySpaced](./get_evenlyspaced/) **false** olarak ayarlanmışsa, her sütun için genişlik ve boşluğu ayrı ayrı belirtmeniz gerekir. Tek tek [TextColumn](../textcolumn/) nesnelerine erişmek için indeksleyiciyi kullanın.

Özel sütun genişlikleri kullanırken, tüm sütun genişliklerinin ve aralarındaki boşlukların toplamının sayfa genişliğinden sol ve sağ sayfa kenar boşlukları çıkarıldıktan sonra kalan değere eşit olduğundan emin olun.

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
