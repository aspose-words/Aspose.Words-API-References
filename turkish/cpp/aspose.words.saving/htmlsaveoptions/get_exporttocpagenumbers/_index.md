---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers yöntemi"
linktitle: "get_ExportTocPageNumbers"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers yöntemi. HTML, MHTML ve EPUB kaydedilirken içindekiler tablosuna sayfa numaralarının yazılıp yazılmayacağını belirtir. Varsayılan değer C++'da false'tur."
type: docs
weight: 29000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_exporttocpagenumbers/
---
## HtmlSaveOptions::get_ExportTocPageNumbers method


HTML, MHTML ve EPUB olarak kaydederken içindekiler tablosuna sayfa numaralarının yazılıp yazılmayacağını belirtir. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers() const
```


## Örnekler



.html'ye bir içindekiler tablosu ile belge kaydederken sayfa numaralarının nasıl gösterileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir içindekiler tablosu ekleyin ve ardından belgeyi "Heading" biçimlendirilmiş paragraflarla doldurun
// stilini içindekiler tablosu giriş olarak alacaktır. Her giriş sol tarafta başlık paragrafını gösterecek,
// ve sağ tarafta başlığı içeren sayfa numarasını.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 1");
builder->Writeln(u"Entry 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 3");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 4");
fieldToc->UpdatePageNumbers();
doc->UpdateFields();

// HTML belgelerinde sayfalar yoktur. Bu belgeyi HTML olarak kaydedersek,
// TOC'mizin gösterdiği sayfa numaraları bir anlam ifade etmeyecek.
// Belgeyi HTML olarak kaydettiğimizde, bu sayfa numaralarını TOC'den çıkarmak için bir SaveOptions nesnesi geçebiliriz.
// "ExportTocPageNumbers" bayrağını "true" olarak ayarlarsak,
// her TOC girişi başlığı, ayırıcıyı ve sayfa numarasını gösterecek, Microsoft Word'deki görünümünü koruyacaktır.
// "ExportTocPageNumbers" bayrağını "false" olarak ayarlarsak,
// kaydetme işlemi hem ayırıcıyı hem de sayfa numarasını atlayacak ve her giriş için başlığı olduğu gibi bırakacaktır.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportTocPageNumbers(exportTocPageNumbers);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTocPageNumbers.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTocPageNumbers.html");

if (exportTocPageNumbers)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<span>Entry 1</span>") + u"<span style=\"width:428.14pt; font-family:'Lucida Console'; font-size:10pt; display:inline-block; -aw-font-family:'Times New Roman'; " + u"-aw-tabstop-align:right; -aw-tabstop-leader:dots; -aw-tabstop-pos:469.8pt\">.......................................................................</span>" + u"<span>2</span>" + u"</p>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<span>Entry 2</span>" + u"</p>"));
}
```

## Ayrıca Bakınız

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
