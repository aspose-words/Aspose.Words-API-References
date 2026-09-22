---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_AllowNegativeIndent metodu"
linktitle: "get_AllowNegativeIndent"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_AllowNegativeIndent metodu. Paragrafların negatif sol ve sağ girintilerinin HTML, MHTML veya EPUB olarak kaydedilirken normalleştirilip getirileceğini belirtir. Varsayılan değer C++'da false'tur."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_allownegativeindent/
---
## HtmlSaveOptions::get_AllowNegativeIndent method


Paragrafların negatif sol ve sağ girintilerinin HTML, MHTML veya EPUB olarak kaydedilirken normalleştirilip normalleştirilmeyeceğini belirtir. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_AllowNegativeIndent() const
```

## Açıklamalar


Negatif girinti izin verilmediğinde, HTML'ye sıfır kenar boşluğu olarak dışa aktarılır. Negatif girinti izin verildiğinde, bir paragraf tarayıcı penceresinin bir kısmının dışına çıkabilir.

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

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
