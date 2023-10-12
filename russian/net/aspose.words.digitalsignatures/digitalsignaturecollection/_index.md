---
title: Class DigitalSignatureCollection
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.DigitalSignatures.DigitalSignatureCollection сорт. Предоставляет доступную только для чтения коллекцию цифровых подписей прикрепленных к документу.
type: docs
weight: 390
url: /ru/net/aspose.words.digitalsignatures/digitalsignaturecollection/
---
## DigitalSignatureCollection class

Предоставляет доступную только для чтения коллекцию цифровых подписей, прикрепленных к документу.

Чтобы узнать больше, посетите[Работа с цифровыми подписями](https://docs.aspose.com/words/net/working-with-digital-signatures/) статья документации.

```csharp
public class DigitalSignatureCollection : IEnumerable<DigitalSignature>
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [DigitalSignatureCollection](digitalsignaturecollection/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.digitalsignatures/digitalsignaturecollection/count/) { get; } | Получает количество элементов, содержащихся в коллекции. |
| [IsValid](../../aspose.words.digitalsignatures/digitalsignaturecollection/isvalid/) { get; } | Возвращает`истинный` если все цифровые подписи в этой коллекции действительны и документ не был подделан Также возвращается`истинный` если нет цифровых подписей. Возвращает`ЛОЖЬ` если хотя бы одна цифровая подпись недействительна. |
| [Item](../../aspose.words.digitalsignatures/digitalsignaturecollection/item/) { get; } | Получает подпись документа по указанному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetEnumerator](../../aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/)() | Возвращает объект перечислителя словаря, который можно использовать для перебора всех элементов коллекции. |

### Примечания

[`DigitalSignatures`](../../aspose.words/document/digitalsignatures/)

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

Показывает, как подписывать документы с помощью сертификатов X.509.

```csharp
// Проверяем, что документ не подписан.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Создайте объект CertificateHolder из файла PKCS12, который мы будем использовать для подписи документа.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Существует два способа сохранить подписанную копию документа в локальной файловой системе:
// 1 — обозначить документ по локальному системному имени файла и сохранить подписанную копию в месте, указанном другим именем файла.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 — Взять документ из потока и сохранить подписанную копию в другой поток.
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

* class [DigitalSignature](../digitalsignature/)
* пространство имен [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../)


