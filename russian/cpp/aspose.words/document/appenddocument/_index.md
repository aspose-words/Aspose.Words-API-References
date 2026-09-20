---
title: "Aspose::Words::Document::AppendDocument метод"
linktitle: "AppendDocument"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::AppendDocument метод. Добавляет указанный документ в конец текущего документа в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words/document/appenddocument/
---
## Document::AppendDocument(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) method


Добавляет указанный документ в конец этого документа.

```cpp
void Aspose::Words::Document::AppendDocument(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | Документ для добавления. |
| importFormatMode | Aspose::Words::ImportFormatMode | Указывает, как объединять конфликтующее форматирование стилей. |

## Примеры



Показывает, как добавить документ в конец другого документа.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
srcDoc->get_FirstSection()->get_Body()->AppendParagraph(u"Source document text. ");

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
dstDoc->get_FirstSection()->get_Body()->AppendParagraph(u"Destination document text. ");

// Добавьте исходный документ к целевому документу, сохраняя его форматирование,
// затем сохраните исходный документ в локальной файловой системе.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting);

dstDoc->Save(get_ArtifactsDir() + u"Document.AppendDocument.docx");
```


Показывает, как добавить все документы из папки в конец шаблонного документа.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Template Document");
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Normal);
builder->Writeln(u"Some content here");

// Добавьте все незашифрованные документы с расширением .doc
// из нашего каталога локальной файловой системы в базовый документ.
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

## См. также

* Class [Document](../)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::AppendDocument(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) method


Добавляет указанный документ в конец этого документа.

```cpp
void Aspose::Words::Document::AppendDocument(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | Документ для добавления. |
| importFormatMode | Aspose::Words::ImportFormatMode | Указывает, как объединять конфликтующее форматирование стилей. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Позволяет задавать параметры, влияющие на форматирование результирующего документа. |

## Примеры



Показывает, как управлять конфликтами стилей списков при добавлении документа.
```cpp
// Загрузите документ с текстом в пользовательском стиле и клонируйте его.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom list numbering.docx");
System::SharedPtr<Aspose::Words::Document> dstDoc = srcDoc->Clone();

// Теперь у нас есть два документа, каждый с одинаковым стилем под названием "CustomStyle".
// Измените цвет текста одного из стилей, чтобы отличить его от другого.
dstDoc->get_Styles()->idx_get(u"CustomStyle")->get_Font()->set_Color(System::Drawing::Color::get_DarkRed());

// Если происходит конфликт стилей списков, примените формат списка из исходного документа.
// Установите свойство "KeepSourceNumbering" в значение "false", чтобы не импортировать номера списков в целевой документ.
// Установите свойство "KeepSourceNumbering" в значение "true", чтобы импортировать все конфликтующие
// нумерацию стилей списков с тем же внешним видом, что и в исходном документе.
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_KeepSourceNumbering(keepSourceNumbering);

// Объединение двух документов, у которых разные стили с одинаковым именем, приводит к конфликту стилей.
// Мы можем указать режим импорта формата при добавлении документов, чтобы решить этот конфликт.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepDifferentStyles, options);
dstDoc->UpdateListLabels();

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.AppendDocumentAndResolveStyles.docx");
```


Показывает, как управлять конфликтами стилей списков при вставке документа.
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

// Если происходит конфликт стилей списков, примените формат списка из исходного документа.
// Установите свойство "KeepSourceNumbering" в значение "false", чтобы не импортировать номера списков в целевой документ.
// Установите свойство "KeepSourceNumbering" в значение "true", чтобы импортировать все конфликтующие
// нумерацию стилей списков с тем же внешним видом, что и в исходном документе.
auto importOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importOptions->set_KeepSourceNumbering(keepSourceNumbering);

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->InsertDocument(attachDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, importOptions);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertDocumentAndResolveStyles.docx");
```


Показывает, как управлять конфликтами стилей списков при добавлении клона документа к самому себе.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");

// Если происходит конфликт стилей списков, примените формат списка из исходного документа.
// Установите свойство "KeepSourceNumbering" в значение "false", чтобы не импортировать номера списков в целевой документ.
// Установите свойство "KeepSourceNumbering" в значение "true", чтобы импортировать все конфликтующие
// нумерацию стилей списков с тем же внешним видом, что и в исходном документе.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->MoveToDocumentEnd();
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_KeepSourceNumbering(keepSourceNumbering);
builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->UpdateListLabels();
```

## См. также

* Class [Document](../)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
