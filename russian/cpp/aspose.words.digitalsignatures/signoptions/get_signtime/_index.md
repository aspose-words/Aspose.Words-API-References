---
title: "Метод Aspose::Words::DigitalSignatures::SignOptions::get_SignTime"
linktitle: "get_SignTime"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DigitalSignatures::SignOptions::get_SignTime. Дата подписи. Значение по умолчанию — текущее время (Now) в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.digitalsignatures/signoptions/get_signtime/
---
## SignOptions::get_SignTime method


Дата подписи. Значение по умолчанию — **current time** (**Now**)

```cpp
System::DateTime Aspose::Words::DigitalSignatures::SignOptions::get_SignTime() const
```


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

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
