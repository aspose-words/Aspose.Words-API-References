---
title: "Aspose::Words::TextColumn sınıfı"
linktitle: "TextColumn"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TextColumn sınıfı. Tek bir metin sütununu temsil eder. TextColumn, TextColumnCollection koleksiyonunun bir üyesidir. TextColumn koleksiyonu, bir belgenin bölümündeki tüm sütunları içerir. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 70000
url: /tr/cpp/aspose.words/textcolumn/
---
## TextColumn class


Tek bir metin sütununu temsil eder. [TextColumn](./), [TextColumnCollection](../textcolumncollection/) koleksiyonunun bir üyesidir. [TextColumn](./) koleksiyonu, bir belgenin bölümündeki tüm sütunları içerir. Daha fazla bilgi için [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/) belge makalesini ziyaret edin.

```cpp
class TextColumn : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_SpaceAfter](./get_spaceafter/)() | Bu sütun ile bir sonraki sütun arasındaki boşluğu nokta cinsinden alır veya ayarlar. Son sütun için gerekli değildir. |
| [get_Width](./get_width/)() | Metin sütununun genişliğini nokta cinsinden alır veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SpaceAfter](./set_spaceafter/)(double) | [Aspose::Words::TextColumn::get_SpaceAfter](./get_spaceafter/) için ayarlayıcı. |
| [set_Width](./set_width/)(double) | [Aspose::Words::TextColumn::get_Width](./get_width/) için ayarlayıcı. |
| static [Type](./type/)() |  |
## Açıklamalar


[TextColumn](./) objects are only used to specify columns with custom width and spacing. If you want the columns in the document to be of equal width, set TextColumns.[EvenlySpaced](../textcolumncollection/get_evenlyspaced/) to **true**.

Yeni bir [TextColumn](./) oluşturulduğunda, genişliği ve boşluğu sıfır olarak ayarlanır.

## Örnekler



Düzensiz aralıklı sütunların nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = pageSetup->get_TextColumns();
columns->set_EvenlySpaced(false);
columns->SetCount(2);

// Sütunları düzenlemek için mevcut olan alan miktarını belirleyin.
double contentWidth = pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin();

ASSERT_NEAR(470.30, contentWidth, 0.01);

// İlk sütunu dar olarak ayarlayın.
System::SharedPtr<Aspose::Words::TextColumn> column = columns->idx_get(0);
column->set_Width(100);
column->set_SpaceAfter(20);

// İkinci sütunu, sayfanın kenar boşlukları içinde mevcut olan kalan alanı alacak şekilde ayarlayın.
column = columns->idx_get(1);
column->set_Width(contentWidth - column->get_Width() - column->get_SpaceAfter());

builder->Writeln(u"Narrow column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Wide column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CustomColumnWidth.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
