---
title: DigitalSignatureCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: Легко извлекайте подписи документов с помощью DigitalSignatureCollection. Получайте доступ к подписям по индексу для упрощения управления документами и повышения эффективности.
type: docs
weight: 40
url: /ru/net/aspose.words.digitalsignatures/digitalsignaturecollection/item/
---
## DigitalSignatureCollection indexer

Получает подпись документа по указанному индексу.

```csharp
public DigitalSignature this[int index] { get; }
```

| Параметр | Описание |
| --- | --- |
| index | Нулевой индекс подписи. |

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

* class [DigitalSignature](../../digitalsignature/)
* class [DigitalSignatureCollection](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../../)
