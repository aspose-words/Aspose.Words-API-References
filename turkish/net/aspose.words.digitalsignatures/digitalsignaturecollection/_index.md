---
title: DigitalSignatureCollection Class
linktitle: DigitalSignatureCollection
articleTitle: DigitalSignatureCollection
second_title: .NET için Aspose.Words
description: Güvenli belge yönetimi için salt okunur dijital imza koleksiyonuna kolay erişim sağlayan Aspose.Words DigitalSignatureCollection sınıfını keşfedin.
type: docs
weight: 590
url: /tr/net/aspose.words.digitalsignatures/digitalsignaturecollection/
---
## DigitalSignatureCollection class

Bir belgeye ekli dijital imzaların salt okunur bir koleksiyonunu sağlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Dijital İmzalarla Çalışın](https://docs.aspose.com/words/net/working-with-digital-signatures/) belgeleme makalesi.

```csharp
public class DigitalSignatureCollection : IEnumerable<DigitalSignature>
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [DigitalSignatureCollection](digitalsignaturecollection/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.digitalsignatures/digitalsignaturecollection/count/) { get; } | Koleksiyonda bulunan öğelerin sayısını alır. |
| [IsValid](../../aspose.words.digitalsignatures/digitalsignaturecollection/isvalid/) { get; } | Geri Döndürür`doğru`bu koleksiyondaki tüm dijital imzalar geçerliyse ve belgede değişiklik yapılmamışsa Ayrıca şunu da döndürür:`doğru` dijital imzalar yoksa. Geri döner`YANLIŞ` en az bir dijital imza geçersizse. |
| [Item](../../aspose.words.digitalsignatures/digitalsignaturecollection/item/) { get; } | Belirtilen dizinde bir belge imzası alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetEnumerator](../../aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilen bir sözlük numaralandırıcı nesnesi döndürür. |

## Notlar

[`DigitalSignatures`](../../aspose.words/document/digitalsignatures/)

## Örnekler

Bir belgedeki her imzaya ilişkin bilgilerin nasıl doğrulanacağını ve görüntüleneceğini gösterir.

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

X.509 sertifikalarıyla belgelerin nasıl imzalanacağını gösterir.

```csharp
// Bir belgenin imzalanmadığını doğrulayın.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Belgeyi imzalamak için kullanacağımız PKCS12 dosyasından bir CertificateHolder nesnesi oluşturalım.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Bir belgenin imzalı bir kopyasını yerel dosya sistemine kaydetmenin iki yolu vardır:
// 1 - Bir belgeyi yerel sistem dosya adıyla tanımlayın ve imzalı bir kopyasını başka bir dosya adıyla belirtilen bir konuma kaydedin.
SignOptions signOptions = new SignOptions { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx",
    certificateHolder, signOptions);

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Bir akıştan bir belge alın ve imzalı bir kopyasını başka bir akışa kaydedin.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Lütfen belgenin tüm dijital imzalarının geçerli olduğunu doğrulayın ve ayrıntılarını kontrol edin.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Ayrıca bakınız

* class [DigitalSignature](../digitalsignature/)
* ad alanı [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../)
