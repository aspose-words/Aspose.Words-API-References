---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode yöntemi"
linktitle: "get_TableWidthOutputMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode yöntemi. Tablo, satır ve hücre genişliklerinin HTML, MHTML veya EPUB'a nasıl dışa aktarıldığını kontrol eder. Varsayılan değer C++'ta All'dir."
type: docs
weight: 47000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_tablewidthoutputmode/
---
## HtmlSaveOptions::get_TableWidthOutputMode method


Tablo, satır ve hücre genişliklerinin HTML, MHTML veya EPUB'a nasıl dışa aktarıldığını kontrol eder. Varsayılan değer [All](../../htmlelementsizeoutputmode/)dir.

```cpp
Aspose::Words::Saving::HtmlElementSizeOutputMode Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode() const
```

## Açıklamalar


HTML formatında, tablo, satır ve hücre öğeleri (**%<table>**, **%<tr>**, **%<th>**, **%<td>**) genişlikleri göreceli (yüzde) ya da mutlak birimlerde belirtilebilir. Aspose.Words'teki bir belgede de tablolar, satırlar ve hücreler genişliklerini aynı şekilde göreceli ya da mutlak birimlerle belirtebilir.

Aspose.Words kullanarak bir belgeyi HTML'ye dönüştürdüğünüzde, tablo, satır ve hücre genişliklerinin nasıl dışa aktarıldığını kontrol etmek isteyebilirsiniz; bu, ortaya çıkan belgenin görsel aracında (ör. bir tarayıcı veya görüntüleyici) nasıl görüntüleneceğini etkiler.

Bu özelliği, hedef belgeye hangi tablo genişliği değerlerinin dışa aktarılacağını belirlemek için bir filtre olarak kullanın. Örneğin, bir belgeyi EPUB'a dönüştürüyor ve belgeyi bir mobil okuma cihazında görüntülemeyi planlıyorsanız, mutlak genişlik değerlerinin dışa aktarılmasından kaçınmak isteyebilirsiniz. Bunu yapmak için çıktı modunu [RelativeOnly](../../htmlelementsizeoutputmode/) veya [None](../../htmlelementsizeoutputmode/) olarak belirtmeniz gerekir; böylece mobil cihazdaki görüntüleyici tabloyu ekranın genişliğine en iyi şekilde sığacak şekilde yerleştirebilir.

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

* Enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
