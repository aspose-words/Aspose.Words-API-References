---
title: "Aspose::Words::FileFormatUtil::DetectFileFormat метод"
linktitle: "DetectFileFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::FileFormatUtil::DetectFileFormat метод. Определяет и возвращает информацию о формате документа, хранящегося в потоке, в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/fileformatutil/detectfileformat/
---
## FileFormatUtil::DetectFileFormat(const System::SharedPtr\<System::IO::Stream\>\&) method


Определяет и возвращает информацию о формате документа, хранящегося в потоке.

```cpp
static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(const System::SharedPtr<System::IO::Stream> &stream)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | Поток. |

### ReturnValue

Объект [FileFormatInfo](../../fileformatinfo/), содержащий обнаруженную информацию.
## Примечания


Поток должен быть установлен в начало документа.

Когда этот метод возвращается, позиция в потоке восстанавливается до исходного положения.

Даже если этот метод определяет формат документа, он не гарантирует, что указанный документ является действительным. Этот метод только определяет формат документа, читая данные, достаточные для определения. Чтобы полностью проверить корректность документа, необходимо загрузить документ в объект [Document](../../document/).

Этот метод бросает [FileCorruptedException](../../filecorruptedexception/), когда формат распознан, но обнаружение не может завершиться из‑за повреждения.

## Примеры



Показывает, как использовать методы [FileFormatUtil](../) для определения формата документа.
```cpp
// Загрузите документ из файла без расширения и затем определите его формат.
{
    System::SharedPtr<System::IO::FileStream> docStream = System::IO::File::OpenRead(get_MyDir() + u"Word document with missing file extension");
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(docStream);
    Aspose::Words::LoadFormat loadFormat = info->get_LoadFormat();

    ASSERT_EQ(Aspose::Words::LoadFormat::Doc, loadFormat);

    // Ниже представлены два метода преобразования LoadFormat в соответствующий SaveFormat.
    // 1 -  Получите строку расширения файла для LoadFormat, затем получите соответствующий SaveFormat из этой строки:
    System::String fileExtension = Aspose::Words::FileFormatUtil::LoadFormatToExtension(loadFormat);
    Aspose::Words::SaveFormat saveFormat = Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(fileExtension);

    // 2 -  Преобразуйте LoadFormat напрямую в его SaveFormat:
    saveFormat = Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(loadFormat);

    // Загрузите документ из потока и затем сохраните его с автоматически определённым расширением файла.
    auto doc = System::MakeObject<Aspose::Words::Document>(docStream);

    ASSERT_EQ(u".doc", Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));

    doc->Save(get_ArtifactsDir() + u"File.SaveToDetectedFileFormat" + Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));
}
```

## См. также

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## FileFormatUtil::DetectFileFormat(const System::String\&) method


Определяет и возвращает информацию о формате документа, хранящегося в дисковом файле.

```cpp
static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(const System::String &fileName)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | const System::String\& | Имя файла. |

### ReturnValue

Объект [FileFormatInfo](../../fileformatinfo/), содержащий обнаруженную информацию.
## Примечания


Даже если этот метод определяет формат документа, он не гарантирует, что указанный документ является действительным. Этот метод только определяет формат документа, читая данные, достаточные для определения. Чтобы полностью проверить корректность документа, необходимо загрузить документ в объект [Document](../../document/).

Этот метод бросает [FileCorruptedException](../../filecorruptedexception/), когда формат распознан, но обнаружение не может завершиться из‑за повреждения.

## Примеры



Показывает, как использовать класс [FileFormatUtil](../) для определения формата документа и шифрования.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Настройте объект SaveOptions для шифрования документа
// с паролем при сохранении, а затем сохраните документ.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(Aspose::Words::SaveFormat::Odt);
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt", saveOptions);

// Проверьте тип файла нашего документа и его статус шифрования.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt");

ASSERT_EQ(u".odt", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_TRUE(info->get_IsEncrypted());
```


Показывает, как использовать класс [FileFormatUtil](../) для определения формата документа и наличия цифровых подписей.
```cpp
// Используйте экземпляр FileFormatInfo, чтобы проверить, что документ не имеет цифровой подписи.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx");

ASSERT_EQ(u".docx", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_FALSE(info->get_HasDigitalSignature());

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx", certificateHolder, signOptions);

// Используйте новый FileFormatInstance, чтобы подтвердить, что он подписан.
info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx");

ASSERT_TRUE(info->get_HasDigitalSignature());

// Мы можем загрузить и получить доступ к подписям подписанного документа в коллекции, как показано ниже.
ASSERT_EQ(1, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx")->get_Count());
```

## См. также

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## FileFormatUtil::DetectFileFormat(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(std::basic_istream<CharType, Traits> &stream)
```

## См. также

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
