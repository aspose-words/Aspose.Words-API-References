---
title: DigitalSignatures
second_title: Справочник по API Aspose.Words для .NET
description: Получает коллекцию цифровых подписей для этого документа и результаты их проверки.
type: docs
weight: 100
url: /ru/net/aspose.words/document/digitalsignatures/
---
## Document.DigitalSignatures property

Получает коллекцию цифровых подписей для этого документа и результаты их проверки.

```csharp
public DigitalSignatureCollection DigitalSignatures { get; }
```

### Примечания

Эта коллекция содержит цифровые подписи, которые были загружены из исходного документа. Эти цифровые подписи не будут сохранены при сохранении этого документа.[`Document`](../../document) object в файл или поток, потому что при сохранении или преобразовании будет создан документ, отличный от исходного , и исходные цифровые подписи больше не будут действительны.

Эта коллекция никогда не бывает нулевой. Если документ не подписан, он будет содержать нулевые элементы.

### Примеры

Показывает, как проверять и отображать информацию о каждой подписи в документе.

```csharp
Document doc = new Document(MyDir + "Digitally signed.docx");

foreach (DigitalSignature signature in doc.DigitalSignatures)
{
    Console.WriteLine($"{(signature.IsValid ? "Valid" : "Invalid")} signature: ");
    Console.WriteLine($"\tReason:\t{signature.Comments}"); 
    Console.WriteLine($"\tType:\t{signature.SignatureType}");
    Console.WriteLine($"\tSign time:\t{signature.SignTime}");
    Console.WriteLine($"\tSubject name:\t{signature.CertificateHolder.Certificate.SubjectName}");
    Console.WriteLine($"\tIssuer name:\t{signature.CertificateHolder.Certificate.IssuerName.Name}");
    Console.WriteLine();
}
```

Показывает, как подписывать документы сертификатами X.509.

```csharp
// Проверяем, что документ не подписан.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Создадим объект CertificateHolder из файла PKCS12, который мы будем использовать для подписи документа.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Есть два способа сохранить подписанную копию документа в локальную файловую систему:
// 1 - Назначить документ именем локального системного файла и сохранить подписанную копию в месте, указанном другим именем файла.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Взять документ из потока и сохранить подписанную копию в другой поток.
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

* class [DigitalSignatureCollection](../../../aspose.words.digitalsignatures/digitalsignaturecollection)
* class [Document](../../document)
* пространство имен [Aspose.Words](../../document)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
