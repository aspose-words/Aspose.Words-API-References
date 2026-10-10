---
title: "Aspose::Words::Document::AppendDocument method"
linktitle: "AppendDocument"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::AppendDocument method. Lägger till det angivna dokumentet i slutet av detta dokument i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/document/appenddocument/
---
## Document::AppendDocument(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) method


Lägger till det angivna dokumentet i slutet av detta dokument.

```cpp
void Aspose::Words::Document::AppendDocument(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | Dokumentet som ska läggas till. |
| importFormatMode | Aspose::Words::ImportFormatMode | Anger hur stilformatering som krockar ska slås samman. |

## Exempel



Visar hur man lägger till ett dokument i slutet av ett annat dokument.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
srcDoc->get_FirstSection()->get_Body()->AppendParagraph(u"Source document text. ");

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
dstDoc->get_FirstSection()->get_Body()->AppendParagraph(u"Destination document text. ");

// Lägg till källdokumentet i destinationsdokumentet samtidigt som dess formatering bevaras,
// spara sedan källdokumentet till det lokala filsystemet.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting);

dstDoc->Save(get_ArtifactsDir() + u"Document.AppendDocument.docx");
```


Visar hur man lägger till alla dokument i en mapp i slutet av ett mall-dokument.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Template Document");
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Normal);
builder->Writeln(u"Some content here");

// Lägg till alla okrypterade dokument med .doc‑tillägget
// från vår lokala filsystemkatalog till basdokumentet.
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

## Se även

* Class [Document](../)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::AppendDocument(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) method


Lägger till det angivna dokumentet i slutet av detta dokument.

```cpp
void Aspose::Words::Document::AppendDocument(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | Dokumentet som ska läggas till. |
| importFormatMode | Aspose::Words::ImportFormatMode | Anger hur stilformatering som krockar ska slås samman. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Tillåter att ange alternativ som påverkar formateringen av ett resultatsdokument. |

## Exempel



Visar hur man hanterar krockar i liststilar när man lägger till ett dokument.
```cpp
// Läs in ett dokument med text i en anpassad stil och klona det.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom list numbering.docx");
System::SharedPtr<Aspose::Words::Document> dstDoc = srcDoc->Clone();

// Vi har nu två dokument, var och en med en identisk stil som heter "CustomStyle".
// Ändra textfärgen för en av stilarna för att särskilja den från den andra.
dstDoc->get_Styles()->idx_get(u"CustomStyle")->get_Font()->set_Color(System::Drawing::Color::get_DarkRed());

// Om det finns en krock mellan liststilar, tillämpa listformatet från källdokumentet.
// Ställ in egenskapen "KeepSourceNumbering" till "false" för att inte importera några listnummer till destinationsdokumentet.
// Ställ in egenskapen "KeepSourceNumbering" till "true" för att importera all krockande
// liststilens numrering med samma utseende som den hade i källdokumentet.
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_KeepSourceNumbering(keepSourceNumbering);

// Att sammanfoga två dokument som har olika stilar med samma namn orsakar en stilkrock.
// Vi kan ange ett importformatläge när vi lägger till dokument för att lösa denna krock.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepDifferentStyles, options);
dstDoc->UpdateListLabels();

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.AppendDocumentAndResolveStyles.docx");
```


Visar hur man hanterar stilkrockar för listor när man infogar ett dokument.
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

// Om det finns en krock mellan liststilar, tillämpa listformatet från källdokumentet.
// Ställ in egenskapen "KeepSourceNumbering" till "false" för att inte importera några listnummer till destinationsdokumentet.
// Ställ in egenskapen "KeepSourceNumbering" till "true" för att importera all krockande
// liststilens numrering med samma utseende som den hade i källdokumentet.
auto importOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importOptions->set_KeepSourceNumbering(keepSourceNumbering);

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->InsertDocument(attachDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, importOptions);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertDocumentAndResolveStyles.docx");
```


Visar hur man hanterar stilkrockar för listor när man lägger till en klon av ett dokument till sig självt.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");

// Om det finns en krock mellan liststilar, tillämpa listformatet från källdokumentet.
// Ställ in egenskapen "KeepSourceNumbering" till "false" för att inte importera några listnummer till destinationsdokumentet.
// Ställ in egenskapen "KeepSourceNumbering" till "true" för att importera all krockande
// liststilens numrering med samma utseende som den hade i källdokumentet.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->MoveToDocumentEnd();
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_KeepSourceNumbering(keepSourceNumbering);
builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->UpdateListLabels();
```

## Se även

* Class [Document](../)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
