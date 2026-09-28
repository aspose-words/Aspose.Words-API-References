---
title: "Aspose::Words::DigitalSignatures::CertificateHolder::Create метод"
linktitle: "Create"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DigitalSignatures::CertificateHolder::Create метод. Создаёт объект CertificateHolder, используя массив байтов хранилища PKCS12 и его пароль в C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.digitalsignatures/certificateholder/create/
---
## CertificateHolder::Create(const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<System::Security::SecureString\>\&) method


Создаёт объект [CertificateHolder](../) используя массив байтов хранилища PKCS12 и его пароль.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::ArrayPtr<uint8_t> &certBytes, const System::SharedPtr<System::Security::SecureString> &password)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| certBytes | const System::ArrayPtr\<uint8_t\>\& | Массив байтов, содержащий данные из сертификата X.509. |
| password | const System::SharedPtr\<System::Security::SecureString\>\& | Пароль, необходимый для доступа к данным сертификата X.509. |

### ReturnValue

Экземпляр [CertificateHolder](../)

## См. также

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::ArrayPtr\<uint8_t\>\&, const System::String\&) method


Создаёт объект [CertificateHolder](../) используя массив байтов хранилища PKCS12 и его пароль.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::ArrayPtr<uint8_t> &certBytes, const System::String &password)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| certBytes | const System::ArrayPtr\<uint8_t\>\& | Массив байтов, содержащий данные из сертификата X.509. |
| password | const System::String\& | Пароль, необходимый для доступа к данным сертификата X.509. |

### ReturnValue

Экземпляр [CertificateHolder](../)

## См. также

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::String\&, const System::String\&) method


Создаёт объект [CertificateHolder](../), используя путь к хранилищу PKCS12 и его пароль.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::String &fileName, const System::String &password)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | const System::String\& | Имя файла сертификата. |
| password | const System::String\& | Пароль, необходимый для доступа к данным сертификата X.509. |

### ReturnValue

Экземпляр [CertificateHolder](../)

## Примеры



Показывает, как цифрово подписывать документы.
```cpp
// Создайте сертификат X.509 из хранилища PKCS#12, которое должно содержать закрытый ключ.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Создайте комментарий и дату, которые будут применены с нашей новой цифровой подписью.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// Возьмите неподписанный документ из локальной файловой системы через файловый поток,
// затем создайте подписанную копию, определяемую именем файла выходного файлового потока.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

## См. также

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::String\&, const System::String\&, const System::String\&) method


Создаёт объект [CertificateHolder](../), используя путь к хранилищу PKCS12, его пароль и псевдоним, с помощью которого будет найден приватный ключ и сертификат.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::String &fileName, const System::String &password, const System::String &alias)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | const System::String\& | Имя файла сертификата. |
| password | const System::String\& | Пароль, необходимый для доступа к данным сертификата X.509. |
| псевдоним | const System::String\& | Связанный псевдоним для сертификата и его приватного ключа |

### ReturnValue

Экземпляр [CertificateHolder](../)

## См. также

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
