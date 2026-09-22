---
title: "Aspose::Words::Saving::HtmlElementSizeOutputMode enum"
linktitle: "HtmlElementSizeOutputMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlElementSizeOutputMode enum. Aspose.Words'in C++'ta öğe genişliklerini ve yüksekliklerini HTML, MHTML ve EPUB formatına nasıl dışa aktardığını belirtir."
type: docs
weight: 58000
url: /tr/cpp/aspose.words.saving/htmlelementsizeoutputmode/
---
## HtmlElementSizeOutputMode enum


Aspose.Words'in öğe genişliklerini ve yüksekliklerini HTML, MHTML ve EPUB'a nasıl dışa aktaracağını belirtir.

```cpp
enum class HtmlElementSizeOutputMode
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Tümü | 0 | Belgede belirtilen, mutlak ve göreceli birimlerdeki tüm öğe boyutları dışa aktarılır. |
| RelativeOnly | 1 | Öğe boyutları yalnızca belgede göreceli birimlerle belirtilmişse dışa aktarılır. Sabit boyutlar bu modda dışa aktarılmaz. Görsel ajanlar, belge düzenini daha doğal hâle getirmek için eksik boyutları hesaplayacaktır. |
| None | 2 | Öğe boyutları dışa aktarılmaz. Görsel ajanlar, öğeler arasındaki ilişkiye göre düzeni otomatik olarak oluşturacaktır. |


## Örnekler



Çıktı .html dosyasında negatif girintileri nasıl koruyacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Negatif girintili bir tablo ekleyin; bu tabloyu sol sayfa sınırının ötesine sola itecektir.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2");
builder->EndTable();
table->set_LeftIndent(-36);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(144));

builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);

// Pozitif girintili bir tablo ekleyin; bu tabloyu sağa itecektir.
table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2");
builder->EndTable();
table->set_LeftIndent(36);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(144));

// Bir belgeyi HTML olarak kaydettiğimizde, Aspose.Words yalnızca negatif girintileri korur
// \"AllowNegativeIndent\" bayrağını ayarlarsak, ilk tabloya uyguladığımız gibi
// \"true\" olarak ayarlayacağımız bir SaveOptions nesnesinde.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_AllowNegativeIndent(allowNegativeIndent);
options->set_TableWidthOutputMode(Aspose::Words::Saving::HtmlElementSizeOutputMode::RelativeOnly);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.NegativeIndent.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.NegativeIndent.html");

if (allowNegativeIndent)
{
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
