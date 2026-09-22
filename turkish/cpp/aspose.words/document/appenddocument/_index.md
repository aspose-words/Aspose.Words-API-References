---
title: "Aspose::Words::Document::AppendDocument yöntemi"
linktitle: "AppendDocument"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::AppendDocument yöntemi. Belirtilen belgeyi bu belgenin sonuna C++ içinde ekler."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/document/appenddocument/
---
## Document::AppendDocument(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) method


Belirtilen belgeyi bu belgenin sonuna ekler.

```cpp
void Aspose::Words::Document::AppendDocument(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | Eklenecek belge. |
| importFormatMode | Aspose::Words::ImportFormatMode | Çakışan stil biçimlendirmesinin nasıl birleştirileceğini belirtir. |

## Örnekler



Bir belgeyi başka bir belgenin sonuna nasıl ekleneceğini gösterir.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
srcDoc->get_FirstSection()->get_Body()->AppendParagraph(u"Source document text. ");

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
dstDoc->get_FirstSection()->get_Body()->AppendParagraph(u"Destination document text. ");

// Kaynak belgeyi, biçimlendirmesini koruyarak hedef belgeye ekleyin,
// daha sonra kaynak belgeyi yerel dosya sistemine kaydedin.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting);

dstDoc->Save(get_ArtifactsDir() + u"Document.AppendDocument.docx");
```


Bir klasördeki tüm belgeleri şablon belgenin sonuna nasıl ekleneceğini gösterir.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Template Document");
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Normal);
builder->Writeln(u"Some content here");

// .doc uzantılı tüm şifrelenmemiş belgeleri ekleyin
// yerel dosya sistemi dizinimizden temel belgeye.
System::SharedPtr<System::Collections::Generic::List<System::String>> docFiles = System::IO::Directory::GetFiles(get_MyDir(), u"*.doc")->LINQ_Where(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String item)>>([](System::String item) -> bool
{
    return item.EndsWith(u".doc");
})))->LINQ_ToList();
for (auto&& fileName : docFiles)
{
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(fileName);
    if (info->get_IsEncrypted())
    {
        continue;
    }

    auto srcDoc = System::MakeObject<Aspose::Words::Document>(fileName);
    dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles);
}

dstDoc->Save(get_ArtifactsDir() + u"Document.AppendAllDocumentsInFolder.doc");
```

## Ayrıca Bakınız

* Class [Document](../)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::AppendDocument(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) method


Belirtilen belgeyi bu belgenin sonuna ekler.

```cpp
void Aspose::Words::Document::AppendDocument(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | Eklenecek belge. |
| importFormatMode | Aspose::Words::ImportFormatMode | Çakışan stil biçimlendirmesinin nasıl birleştirileceğini belirtir. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Sonuç belgesinin biçimlendirmesini etkileyen seçenekleri belirtmeye olanak tanır. |

## Örnekler



Bir belgeyi eklerken liste stili çakışmalarını nasıl yöneteceğinizi gösterir.
```cpp
// Özel bir stilde metin içeren bir belgeyi yükleyin ve klonlayın.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom list numbering.docx");
System::SharedPtr<Aspose::Words::Document> dstDoc = srcDoc->Clone();

// Şimdi her biri "CustomStyle" adlı aynı stile sahip iki belgemiz var.
// Stillerden birinin metin rengini değiştirerek diğerinden ayırın.
dstDoc->get_Styles()->idx_get(u"CustomStyle")->get_Font()->set_Color(System::Drawing::Color::get_DarkRed());

// Liste stilleri çakışıyorsa, kaynak belgenin liste biçimini uygulayın.
// "KeepSourceNumbering" özelliğini "false" olarak ayarlayarak hedef belgeye herhangi bir liste numarası ithal etmeyin.
// "KeepSourceNumbering" özelliğini "true" olarak ayarlayarak tüm çakışan
// liste stili numaralandırmasını, kaynak belgede olduğu gibi aynı görünüme sahip şekilde ithal edin.
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_KeepSourceNumbering(keepSourceNumbering);

// Aynı adı paylaşan farklı stillere sahip iki belgeyi birleştirmek stil çakışmasına neden olur.
// Bu çakışmayı çözmek için belgeleri eklerken bir içe aktarma biçim modu belirtebiliriz.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepDifferentStyles, options);
dstDoc->UpdateListLabels();

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.AppendDocumentAndResolveStyles.docx");
```


Bir belgeyi eklerken liste stili çakışmalarını nasıl yöneteceğinizi gösterir.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);

dstDoc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);
System::SharedPtr<Aspose::Words::Lists::List> list = dstDoc->get_Lists()->idx_get(0);

builder->get_ListFormat()->set_List(list);

for (int32_t i = 1; i <= 15; i++)
{
    builder->Write(System::String::Format(u"List Item {0}\n", i));
}

auto attachDoc = System::ExplicitCast<Aspose::Words::Document>(System::ExplicitCast<Aspose::Words::Node>(dstDoc)->Clone(true));

// Liste stilleri çakışıyorsa, kaynak belgenin liste biçimini uygulayın.
// "KeepSourceNumbering" özelliğini "false" olarak ayarlayarak hedef belgeye herhangi bir liste numarası ithal etmeyin.
// "KeepSourceNumbering" özelliğini "true" olarak ayarlayarak tüm çakışan
// liste stili numaralandırmasını, kaynak belgede olduğu gibi aynı görünüme sahip şekilde ithal edin.
auto importOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importOptions->set_KeepSourceNumbering(keepSourceNumbering);

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->InsertDocument(attachDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, importOptions);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertDocumentAndResolveStyles.docx");
```


Bir belgenin klonunu kendisine eklerken liste stili çakışmalarını nasıl yöneteceğinizi gösterir.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");

// Liste stilleri çakışıyorsa, kaynak belgenin liste biçimini uygulayın.
// "KeepSourceNumbering" özelliğini "false" olarak ayarlayarak hedef belgeye herhangi bir liste numarası ithal etmeyin.
// "KeepSourceNumbering" özelliğini "true" olarak ayarlayarak tüm çakışan
// liste stili numaralandırmasını, kaynak belgede olduğu gibi aynı görünüme sahip şekilde ithal edin.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->MoveToDocumentEnd();
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_KeepSourceNumbering(keepSourceNumbering);
builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->UpdateListLabels();
```

## Ayrıca Bakınız

* Class [Document](../)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
