---
title: "Aspose::Words::DigitalSignatures::SignOptions::get_SignTime Methode"
linktitle: "get_SignTime"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DigitalSignatures::SignOptions::get_SignTime Methode. Das Datum der Signatur. Der Standardwert ist die aktuelle Zeit (Now) in C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words.digitalsignatures/signoptions/get_signtime/
---
## SignOptions::get_SignTime method


Das Datum der Unterzeichnung. Standardwert ist **current time** (**Now**)

```cpp
System::DateTime Aspose::Words::DigitalSignatures::SignOptions::get_SignTime() const
```


## Beispiele



Zeigt, wie man Dokumente digital signiert.
```cpp
// Erstellen Sie ein X.509-Zertifikat aus einem PKCS#12-Store, der einen privaten Schlüssel enthalten sollte.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Erstellen Sie einen Kommentar und ein Datum, die mit unserer neuen digitalen Signatur angewendet werden.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// Nehmen Sie ein unsigniertes Dokument aus dem lokalen Dateisystem über einen Dateistream,
// und erstellen Sie dann eine signierte Kopie davon, bestimmt durch den Dateinamen des Ausgabedateistreams.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

## Siehe auch

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
