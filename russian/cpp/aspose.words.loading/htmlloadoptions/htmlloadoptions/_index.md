---
title: "Конструктор Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions"
linktitle: "HtmlLoadOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Конструктор Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions. Инициализирует новый экземпляр этого класса со значениями по умолчанию в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.loading/htmlloadoptions/htmlloadoptions/
---
## HtmlLoadOptions::HtmlLoadOptions() constructor


Инициализирует новый экземпляр этого класса со значениями по умолчанию.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions()
```


## Примеры



Показывает, как поддерживать условные комментарии при загрузке HTML‑документа.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// Если значение истинно, то мы учитываем код VML при разборе загруженного документа.
loadOptions->set_SupportVml(supportVml);

// Этот документ содержит JPEG‑изображение внутри тегов "<!--[if gte vml 1]>",
// и другое PNG‑изображение внутри тегов "<![if !vml]>".
// Если установить флаг "SupportVml" в значение "true", то Aspose.Words загрузит JPEG.
// Если установить этот флаг в значение "false", то Aspose.Words загрузит только PNG.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```

## См. также

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## HtmlLoadOptions::HtmlLoadOptions(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) constructor


Сокращение для инициализации нового экземпляра этого класса со свойствами, установленными в указанные значения.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions(Aspose::Words::LoadFormat loadFormat, const System::String &password, const System::String &baseUri)
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
* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## HtmlLoadOptions::HtmlLoadOptions(const System::String\&) constructor


Сокращение для инициализации нового экземпляра этого класса с указанным паролем для загрузки зашифрованного документа.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions(const System::String &password)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| password | const System::String\& | Пароль для открытия зашифрованного документа. Может быть **null** или пустой строкой. |

## Примеры



Показывает, как зашифровать HTML‑документ, а затем открыть его с помощью пароля.
```cpp
// Создайте и подпишите зашифрованный HTML‑документ из зашифрованного .docx.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"HtmlLoadOptions.EncryptedHtml.html";
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);

// Чтобы загрузить и прочитать этот документ, нам потребуется передать его расшифровку
// пароль, используя объект HtmlLoadOptions.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(u"docPassword");

ASSERT_EQ(signOptions->get_DecryptionPassword(), loadOptions->get_Password());

auto doc = System::MakeObject<Aspose::Words::Document>(outputFileName, loadOptions);

ASSERT_EQ(u"Test encrypted document.", doc->GetText().Trim());
```

## См. также

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
