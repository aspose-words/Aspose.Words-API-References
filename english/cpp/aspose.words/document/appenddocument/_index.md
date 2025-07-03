---
title: Aspose::Words::Document::AppendDocument method
linktitle: AppendDocument
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::AppendDocument method. Appends the specified document to the end of this document in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words/document/appenddocument/
---
## Document::AppendDocument(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) method


Appends the specified document to the end of this document.

```cpp
void Aspose::Words::Document::AppendDocument(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode)
```


| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | The document to append. |
| importFormatMode | Aspose::Words::ImportFormatMode | Specifies how to merge style formatting that clashes. |

## Examples



Shows how to append a document to the end of another document. 
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
srcDoc->get_FirstSection()->get_Body()->AppendParagraph(u"Source document text. ");

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
dstDoc->get_FirstSection()->get_Body()->AppendParagraph(u"Destination document text. ");

// Append the source document to the destination document while preserving its formatting,
// then save the source document to the local file system.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting);

dstDoc->Save(get_ArtifactsDir() + u"Document.AppendDocument.docx");
```


Shows how to append all the documents in a folder to the end of a template document. 
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Template Document");
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Normal);
builder->Writeln(u"Some content here");

// Append all unencrypted documents with the .doc extension
// from our local file system directory to the base document.
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

## See Also

* Class [Document](../)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::AppendDocument(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) method


Appends the specified document to the end of this document.

```cpp
void Aspose::Words::Document::AppendDocument(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | The document to append. |
| importFormatMode | Aspose::Words::ImportFormatMode | Specifies how to merge style formatting that clashes. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Allows to specify options that affect formatting of a result document. |

## Examples



Shows how to manage list style clashes while appending a document. 
```cpp
// Load a document with text in a custom style and clone it.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom list numbering.docx");
System::SharedPtr<Aspose::Words::Document> dstDoc = srcDoc->Clone();

// We now have two documents, each with an identical style named "CustomStyle".
// Change the text color for one of the styles to set it apart from the other.
dstDoc->get_Styles()->idx_get(u"CustomStyle")->get_Font()->set_Color(System::Drawing::Color::get_DarkRed());

// If there is a clash of list styles, apply the list format of the source document.
// Set the "KeepSourceNumbering" property to "false" to not import any list numbers into the destination document.
// Set the "KeepSourceNumbering" property to "true" import all clashing
// list style numbering with the same appearance that it had in the source document.
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_KeepSourceNumbering(keepSourceNumbering);

// Joining two documents that have different styles that share the same name causes a style clash.
// We can specify an import format mode while appending documents to resolve this clash.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepDifferentStyles, options);
dstDoc->UpdateListLabels();

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.AppendDocumentAndResolveStyles.docx");
```


Shows how to manage list style clashes while inserting a document. 
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

// If there is a clash of list styles, apply the list format of the source document.
// Set the "KeepSourceNumbering" property to "false" to not import any list numbers into the destination document.
// Set the "KeepSourceNumbering" property to "true" import all clashing
// list style numbering with the same appearance that it had in the source document.
auto importOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importOptions->set_KeepSourceNumbering(keepSourceNumbering);

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->InsertDocument(attachDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, importOptions);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertDocumentAndResolveStyles.docx");
```


Shows how to manage list style clashes while appending a clone of a document to itself. 
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");

// If there is a clash of list styles, apply the list format of the source document.
// Set the "KeepSourceNumbering" property to "false" to not import any list numbers into the destination document.
// Set the "KeepSourceNumbering" property to "true" import all clashing
// list style numbering with the same appearance that it had in the source document.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->MoveToDocumentEnd();
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_KeepSourceNumbering(keepSourceNumbering);
builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->UpdateListLabels();
```

## See Also

* Class [Document](../)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
