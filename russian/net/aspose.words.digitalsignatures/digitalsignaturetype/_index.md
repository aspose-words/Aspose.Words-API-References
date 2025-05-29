---
title: DigitalSignatureType Enum
linktitle: DigitalSignatureType
articleTitle: DigitalSignatureType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.DigitalSignatures.DigitalSignatureType, чтобы повысить безопасность ваших документов с помощью универсальных возможностей цифровой подписи.
type: docs
weight: 600
url: /ru/net/aspose.words.digitalsignatures/digitalsignaturetype/
---
## DigitalSignatureType enumeration

Указывает тип цифровой подписи.

```csharp
public enum DigitalSignatureType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Unknown | `0` | Указывает на ошибку, неизвестный тип цифровой подписи. |
| CryptoApi | `1` | Метод подписи Crypto API, используемый в двоичных документах Microsoft Word 97-2003 .DOC. |
| XmlDsig | `2` | Метод подписи XmlDsig, используемый в документах OOXML и OpenDocument. |

## Примеры

Показывает, как подписывать документы с помощью сертификатов X.509.

```csharp
// Убедитесь, что документ не подписан.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Создаем объект CertificateHolder из файла PKCS12, который будем использовать для подписи документа.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Существует два способа сохранения подписанной копии документа в локальной файловой системе:
// 1 — Обозначить документ именем файла локальной системы и сохранить подписанную копию в месте, указанном другим именем файла.
SignOptions signOptions = new SignOptions { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx",
    certificateHolder, signOptions);

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Взять документ из потока и сохранить подписанную копию в другом потоке.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Убедитесь, что все цифровые подписи документа действительны, и проверьте их данные.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Смотрите также

* пространство имен [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../)
