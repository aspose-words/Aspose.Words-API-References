---
title: "Конструктор Aspose::Words::Document::Document"
linktitle: "Document"
second_title: "Справочник API Aspose.Words для C++"
description: "Конструктор Aspose::Words::Document::Document. Создаёт пустой документ Word в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/document/document/
---
## Document::Document() constructor


Создаёт пустой документ Word.

```cpp
Aspose::Words::Document::Document()
```

## Примечания


Пустой документ извлекается из ресурсов, и по умолчанию полученный документ выглядит так, как будто он создан в [Word2007](../../../aspose.words.settings/mswordversion/). Этот пустой документ содержит таблицу шрифтов по умолчанию, минимальный набор стилей по умолчанию и скрытые стили.

[OptimizeFor()](../../../aspose.words.settings/compatibilityoptions/optimizefor/) method can be used to optimize the document contents as well as default Aspose.Words behavior to a particular version of MS Word.

Размер бумаги документа по умолчанию — Letter. Если вы хотите изменить параметры страницы, используйте [PageSetup](../../section/get_pagesetup/).

После создания вы можете использовать [DocumentBuilder](../../documentbuilder/) для лёгкого добавления содержимого документа.

## Примеры



Показывает, как создать простой документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Новые объекты Document по умолчанию поставляются с минимальным набором узлов
// необходимы для начала добавления содержимого, такого как текст и фигуры: Section, Body и Paragraph.
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```


Показывает, как создавать и загружать документы.
```cpp
// Существует два способа создания объекта Document с использованием Aspose.Words.
// 1 -  Создать пустой документ:
auto doc = System::MakeObject<Aspose::Words::Document>();

// Новые объекты Document по умолчанию поставляются с минимальным набором узлов
// необходимы для начала добавления содержимого, такого как текст и фигуры: Section, Body и Paragraph.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// 2 -  Загрузить документ, существующий в локальной файловой системе:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Загруженные документы будут содержать данные, к которым мы можем получить доступ и редактировать их.
ASSERT_EQ(u"Hello World!", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());

// Некоторые операции, которые необходимо выполнить во время загрузки, такие как использование пароля для расшифровки документа,
// можно выполнить, передав объект LoadOptions при загрузке документа.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword"));

ASSERT_EQ(u"Test encrypted document.", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```


Показывает, как форматировать run текста, используя его свойство font.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::SharedPtr\<System::IO::Stream\>\&) constructor


Открывает существующий документ из потока. Автоматически определяет формат файла.

```cpp
Aspose::Words::Document::Document(const System::SharedPtr<System::IO::Stream> &stream)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | Поток, из которого загружать документ. |
## Примечания


Документ должен быть размещён в начале потока. Поток должен поддерживать произвольное позиционирование.

## Примеры



Показывает, как загрузить документ, используя поток.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.docx");
    auto doc = System::MakeObject<Aspose::Words::Document>(stream);

    ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", doc->GetText().Trim());
}
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Открывает существующий документ из потока. Позволяет указывать дополнительные параметры, такие как пароль шифрования.

```cpp
Aspose::Words::Document::Document(const System::SharedPtr<System::IO::Stream> &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | Поток, из которого загружать документ. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Дополнительные параметры, используемые при загрузке документа. Может быть **null**. |
## Примечания


Документ должен быть размещён в начале потока. Поток должен поддерживать произвольное позиционирование.

## Примеры



Показывает, как открыть HTML‑документ с изображениями из потока, используя базовый URI.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.html");
    // Передайте URI базовой папки при загрузке.
    // чтобы любые изображения с относительными URI в HTML‑документе могли быть найдены.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_BaseUri(get_ImageDir());

    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Убедитесь, что первая фигура документа содержит действительное изображение.
    auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(System::TestTools::IsNull(shape->get_ImageData()->get_ImageBytes()));
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```


Показывает, как загрузить зашифрованный документ Microsoft Word.
```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// Aspose.Words генерирует исключение, если попытаться открыть зашифрованный документ без пароля.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx");
})(), Aspose::Words::IncorrectPasswordException);

// При загрузке такого документа пароль передаётся конструктору документа с помощью объекта LoadOptions.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// Существует два способа загрузить зашифрованный документ с объектом LoadOptions.
// 1 -  Загрузить документ из локальной файловой системы по имени файла:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  Загрузить документ из потока:
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```

## См. также

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::String\&) constructor


Открывает существующий документ из файла. Автоматически определяет формат файла.

```cpp
Aspose::Words::Document::Document(const System::String &fileName)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | const System::String\& | Имя файла документа для открытия. |

## Примеры



Показывает, как открыть документ и преобразовать его в .PDF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToPdf.pdf");
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Открывает существующий документ из файла. Позволяет указывать дополнительные параметры, такие как пароль шифрования.

```cpp
Aspose::Words::Document::Document(const System::String &fileName, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | const System::String\& | Имя файла документа для открытия. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Дополнительные параметры, используемые при загрузке документа. Может быть **null**. |

## Примеры



Показывает, как создавать и загружать документы.
```cpp
// Существует два способа создания объекта Document с использованием Aspose.Words.
// 1 -  Создать пустой документ:
auto doc = System::MakeObject<Aspose::Words::Document>();

// Новые объекты Document по умолчанию поставляются с минимальным набором узлов
// необходимы для начала добавления содержимого, такого как текст и фигуры: Section, Body и Paragraph.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// 2 -  Загрузить документ, существующий в локальной файловой системе:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Загруженные документы будут содержать данные, к которым мы можем получить доступ и редактировать их.
ASSERT_EQ(u"Hello World!", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());

// Некоторые операции, которые необходимо выполнить во время загрузки, такие как использование пароля для расшифровки документа,
// можно выполнить, передав объект LoadOptions при загрузке документа.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword"));

ASSERT_EQ(u"Test encrypted document.", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```


Показывает, как загрузить зашифрованный документ Microsoft Word.
```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// Aspose.Words генерирует исключение, если попытаться открыть зашифрованный документ без пароля.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx");
})(), Aspose::Words::IncorrectPasswordException);

// При загрузке такого документа пароль передаётся конструктору документа с помощью объекта LoadOptions.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// Существует два способа загрузить зашифрованный документ с объектом LoadOptions.
// 1 -  Загрузить документ из локальной файловой системы по имени файла:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  Загрузить документ из потока:
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```

## См. также

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(std::istream\&) constructor




```cpp
Aspose::Words::Document::Document(std::istream &stream)
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor




```cpp
Aspose::Words::Document::Document(std::istream &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```

## См. также

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
