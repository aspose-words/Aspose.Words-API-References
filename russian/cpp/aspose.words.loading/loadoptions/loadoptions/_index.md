---
title: "Aspose::Words::Loading::LoadOptions::LoadOptions конструктор"
linktitle: "LoadOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Loading::LoadOptions::LoadOptions конструктор. Инициализирует новый экземпляр этого класса со значениями по умолчанию в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions::LoadOptions() constructor


Инициализирует новый экземпляр этого класса со значениями по умолчанию.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions()
```


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

## См. также

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## LoadOptions::LoadOptions(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) constructor


Сокращение для инициализации нового экземпляра этого класса со свойствами, установленными в указанные значения.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions(Aspose::Words::LoadFormat loadFormat, const System::String &password, const System::String &baseUri)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| loadFormat | Aspose::Words::LoadFormat | Формат загружаемого документа. |
| password | const System::String\& | Пароль для открытия зашифрованного документа. Может быть **null** или пустой строкой. |
| baseUri | const System::String\& | Строка, которая будет использоваться для преобразования относительных URI в абсолютные. Может быть **null** или пустой строкой. |

## Примеры



Показывает, как указать базовый URI при открытии HTML‑документа.
```cpp
// Предположим, что мы хотим загрузить .html‑документ, содержащий изображение, связанное относительным URI
// в то время как изображение находится в другом месте. В этом случае нам потребуется преобразовать относительный URI в абсолютный.
// Мы можем задать базовый URI, используя объект HtmlLoadOptions.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// Хотя изображение было повреждено во входном .html, наш пользовательский базовый URI помог нам восстановить ссылку.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// Этот выходной документ отобразит отсутствующее изображение.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## См. также

* Enum [LoadFormat](../../../aspose.words/loadformat/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## LoadOptions::LoadOptions(const System::String\&) constructor


Сокращение для инициализации нового экземпляра этого класса с указанным паролем для загрузки зашифрованного документа.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions(const System::String &password)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| password | const System::String\& | Пароль для открытия зашифрованного документа. Может быть **null** или пустой строкой. |

## Примеры



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

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
