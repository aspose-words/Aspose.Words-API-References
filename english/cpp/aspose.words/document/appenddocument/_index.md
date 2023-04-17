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
auto srcDoc = MakeObject<Document>();
srcDoc->get_FirstSection()->get_Body()->AppendParagraph(u"Source document text. ");

auto dstDoc = MakeObject<Document>();
dstDoc->get_FirstSection()->get_Body()->AppendParagraph(u"Destination document text. ");

// Append the source document to the destination document while preserving its formatting,
// then save the source document to the local file system.
dstDoc->AppendDocument(srcDoc, ImportFormatMode::KeepSourceFormatting);

dstDoc->Save(ArtifactsDir + u"Document.AppendDocument.docx");
```


Shows how to append all the documents in a folder to the end of a template document. 
```cpp
auto dstDoc = MakeObject<Document>();

auto builder = MakeObject<DocumentBuilder>(dstDoc);
builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading1);
builder->Writeln(u"Template Document");
builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Normal);
builder->Writeln(u"Some content here");

// Append all unencrypted documents with the .doc extension
// from our local file system directory to the base document.
auto isDocFile = [](String item)
{
    return item.EndsWith(u".doc");
};

SharedPtr<System::Collections::Generic::List<String>> docFiles = System::IO::Directory::GetFiles(MyDir, u"*.doc")->LINQ_Where(isDocFile)->LINQ_ToList();
for (const auto& fileName : docFiles)
{
    SharedPtr<FileFormatInfo> info = FileFormatUtil::DetectFileFormat(fileName);
    if (info->get_IsEncrypted())
    {
        continue;
    }

    auto srcDoc = MakeObject<Document>(fileName);
    dstDoc->AppendDocument(srcDoc, ImportFormatMode::UseDestinationStyles);
}

dstDoc->Save(ArtifactsDir + u"Document.AppendAllDocumentsInFolder.doc");
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
auto srcDoc = MakeObject<Document>(MyDir + u"Custom list numbering.docx");
SharedPtr<Document> dstDoc = srcDoc->Clone();

// We now have two documents, each with an identical style named "CustomStyle".
// Change the text color for one of the styles to set it apart from the other.
dstDoc->get_Styles()->idx_get(u"CustomStyle")->get_Font()->set_Color(System::Drawing::Color::get_DarkRed());

// If there is a clash of list styles, apply the list format of the source document.
// Set the "KeepSourceNumbering" property to "false" to not import any list numbers into the destination document.
// Set the "KeepSourceNumbering" property to "true" import all clashing
// list style numbering with the same appearance that it had in the source document.
auto options = MakeObject<ImportFormatOptions>();
options->set_KeepSourceNumbering(keepSourceNumbering);

// Joining two documents that have different styles that share the same name causes a style clash.
// We can specify an import format mode while appending documents to resolve this clash.
dstDoc->AppendDocument(srcDoc, ImportFormatMode::KeepDifferentStyles, options);
dstDoc->UpdateListLabels();

dstDoc->Save(ArtifactsDir + u"DocumentBuilder.AppendDocumentAndResolveStyles.docx");
```


Shows how to manage list style clashes while inserting a document. 
```cpp
auto dstDoc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(dstDoc);
builder->InsertBreak(BreakType::ParagraphBreak);

dstDoc->get_Lists()->Add(ListTemplate::NumberDefault);
SharedPtr<Aspose::Words::Lists::List> list = dstDoc->get_Lists()->idx_get(0);

builder->get_ListFormat()->set_List(list);

for (int i = 1; i <= 15; i++)
{
    builder->Write(String::Format(u"List Item {0}\n", i));
}

auto attachDoc = System::DynamicCast<Document>(dstDoc->Clone(true));

// If there is a clash of list styles, apply the list format of the source document.
// Set the "KeepSourceNumbering" property to "false" to not import any list numbers into the destination document.
// Set the "KeepSourceNumbering" property to "true" import all clashing
// list style numbering with the same appearance that it had in the source document.
auto importOptions = MakeObject<ImportFormatOptions>();
importOptions->set_KeepSourceNumbering(keepSourceNumbering);

builder->InsertBreak(BreakType::SectionBreakNewPage);
builder->InsertDocument(attachDoc, ImportFormatMode::KeepSourceFormatting, importOptions);

dstDoc->Save(ArtifactsDir + u"DocumentBuilder.InsertDocumentAndResolveStyles.docx");
```


Shows how to manage list style clashes while appending a clone of a document to itself. 
```cpp
auto srcDoc = MakeObject<Document>(MyDir + u"List item.docx");
auto dstDoc = MakeObject<Document>(MyDir + u"List item.docx");

// If there is a clash of list styles, apply the list format of the source document.
// Set the "KeepSourceNumbering" property to "false" to not import any list numbers into the destination document.
// Set the "KeepSourceNumbering" property to "true" import all clashing
// list style numbering with the same appearance that it had in the source document.
auto builder = MakeObject<DocumentBuilder>(dstDoc);
builder->MoveToDocumentEnd();
builder->InsertBreak(BreakType::SectionBreakNewPage);

auto options = MakeObject<ImportFormatOptions>();
options->set_KeepSourceNumbering(keepSourceNumbering);
builder->InsertDocument(srcDoc, ImportFormatMode::KeepSourceFormatting, options);

dstDoc->UpdateListLabels();
```

## See Also

* Class [Document](../)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
