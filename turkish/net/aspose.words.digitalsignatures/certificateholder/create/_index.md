---
title: CertificateHolder.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words for .NET
description: CertificateHolder Create yöntem. OluştururCertificateHolder PKCS12 deposunun bayt dizisini ve parolasını kullanan nesne C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words.digitalsignatures/certificateholder/create/
---
## Create(*byte[], SecureString*) {#create}

Oluşturur[`CertificateHolder`](../) PKCS12 deposunun bayt dizisini ve parolasını kullanan nesne.

```csharp
public static CertificateHolder Create(byte[] certBytes, SecureString password)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| certBytes | Byte[] | X.509 sertifikasından verileri içeren bir bayt dizisi. |
| password | SecureString | X.509 sertifika verilerine erişmek için gereken şifre. |

### Geri dönüş değeri

Bir örneği[`CertificateHolder`](../)

### istisnalar

| istisna | şart |
| --- | --- |
| InvalidParameterException | Eğer atılırsa*certBytes* dır-dir`hükümsüz` |
| InvalidParameterException | Eğer atılırsa*password* dır-dir`hükümsüz` |
| SecurityException | PKCS12 deposunda takma ad yoksa atılır |
| IOException | Yanlış şifre veya bozuk dosya varsa atılır. |

## Örnekler

SertifikaHolder nesnelerinin nasıl oluşturulacağını gösterir.

```csharp
// Aşağıda SertifikaHolder nesneleri oluşturmanın dört yolu verilmiştir.
// 1 - Bir PKCS #12 dosyasını bayt dizisine yükleyin ve şifresini uygulayın:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Bir bayt dizisine PKCS #12 dosyasını yükleyin ve güvenli bir parola uygulayın:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Sertifikanın takma adlara karşılık gelen özel anahtarları varsa,
// ilgili anahtarları almak için takma adları kullanabiliriz. Öncelikle geçerli takma adları kontrol edeceğiz.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12StoreBuilder().Build();
    pkcs12Store.Load(certStream, "aw".ToCharArray());
    IEnumerator enumerator = pkcs12Store.Aliases.GetEnumerator();

    while (enumerator.MoveNext())
    {
        if (enumerator.Current != null)
        {
            string currentAlias = enumerator.Current.ToString();
            if (pkcs12Store.IsKeyEntry(currentAlias) && pkcs12Store.GetKey(currentAlias).Key.IsPrivate)
            {
                Console.WriteLine($"Valid alias found: {enumerator.Current}");
            }
        }
    }
}

// 3 - Geçerli bir takma ad kullanın:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Özel anahtar döndüren ilk mevcut takma adı kullanmak için takma ad olarak "null"u iletin:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Ayrıca bakınız

* class [CertificateHolder](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)

---

## Create(*byte[], string*) {#create_1}

Oluşturur[`CertificateHolder`](../) PKCS12 deposunun bayt dizisini ve parolasını kullanan nesne.

```csharp
public static CertificateHolder Create(byte[] certBytes, string password)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| certBytes | Byte[] | X.509 sertifikasından verileri içeren bir bayt dizisi. |
| password | String | X.509 sertifika verilerine erişmek için gereken şifre. |

### Geri dönüş değeri

Bir örneği[`CertificateHolder`](../)

### istisnalar

| istisna | şart |
| --- | --- |
| InvalidParameterException | Eğer atılırsa*certBytes* dır-dir`hükümsüz` |
| InvalidParameterException | Eğer atılırsa*password* dır-dir`hükümsüz` |
| SecurityException | PKCS12 deposunda takma ad yoksa atılır |
| IOException | Yanlış şifre veya bozuk dosya varsa atılır. |

## Örnekler

SertifikaHolder nesnelerinin nasıl oluşturulacağını gösterir.

```csharp
// Aşağıda SertifikaHolder nesneleri oluşturmanın dört yolu verilmiştir.
// 1 - Bir PKCS #12 dosyasını bayt dizisine yükleyin ve şifresini uygulayın:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Bir bayt dizisine PKCS #12 dosyasını yükleyin ve güvenli bir parola uygulayın:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Sertifikanın takma adlara karşılık gelen özel anahtarları varsa,
// ilgili anahtarları almak için takma adları kullanabiliriz. Öncelikle geçerli takma adları kontrol edeceğiz.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12StoreBuilder().Build();
    pkcs12Store.Load(certStream, "aw".ToCharArray());
    IEnumerator enumerator = pkcs12Store.Aliases.GetEnumerator();

    while (enumerator.MoveNext())
    {
        if (enumerator.Current != null)
        {
            string currentAlias = enumerator.Current.ToString();
            if (pkcs12Store.IsKeyEntry(currentAlias) && pkcs12Store.GetKey(currentAlias).Key.IsPrivate)
            {
                Console.WriteLine($"Valid alias found: {enumerator.Current}");
            }
        }
    }
}

// 3 - Geçerli bir takma ad kullanın:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Özel anahtar döndüren ilk mevcut takma adı kullanmak için takma ad olarak "null"u iletin:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Ayrıca bakınız

* class [CertificateHolder](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)

---

## Create(*string, string*) {#create_2}

Oluşturur[`CertificateHolder`](../) PKCS12 deposunun yolunu ve şifresini kullanan nesne.

```csharp
public static CertificateHolder Create(string fileName, string password)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Bir sertifika dosyasının adı. |
| password | String | X.509 sertifika verilerine erişmek için gereken şifre. |

### Geri dönüş değeri

Bir örneği[`CertificateHolder`](../)

### istisnalar

| istisna | şart |
| --- | --- |
| InvalidParameterException | Eğer atılırsa*fileName* dır-dir`hükümsüz` |
| InvalidParameterException | Eğer atılırsa*password* dır-dir`hükümsüz` |
| SecurityException | PKCS12 deposunda takma ad yoksa atılır |
| IOException | Yanlış şifre veya bozuk dosya varsa atılır. |

## Örnekler

Belgelerin dijital olarak nasıl imzalanacağını gösterir.

```csharp
// PKCS#12 deposundan özel anahtar içermesi gereken bir X.509 sertifikası oluşturun.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Yeni dijital imzamızla uygulanacak bir yorum ve tarih oluşturun.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// İmzasız bir belgeyi dosya akışı aracılığıyla yerel dosya sisteminden alın,
// ardından çıktı dosyası akışının dosya adına göre belirlenen imzalı bir kopyasını oluşturun.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Ayrıca bakınız

* class [CertificateHolder](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)

---

## Create(*string, string, string*) {#create_3}

Oluşturur[`CertificateHolder`](../) PKCS12 deposunun yolunu, şifresini ve takma adını kullanarak hangi özel anahtar ve sertifikanın bulunacağını kullanan nesne.

```csharp
public static CertificateHolder Create(string fileName, string password, string alias)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Bir sertifika dosyasının adı. |
| password | String | X.509 sertifika verilerine erişmek için gereken şifre. |
| alias | String | Bir sertifika ve özel anahtarı için ilişkili takma ad |

### Geri dönüş değeri

Bir örneği[`CertificateHolder`](../)

### istisnalar

| istisna | şart |
| --- | --- |
| InvalidParameterException | Eğer atılırsa*fileName* dır-dir`hükümsüz` |
| InvalidParameterException | Eğer atılırsa*password* dır-dir`hükümsüz` |
| SecurityException | PKCS12 deposunda takma ad yoksa atılır |
| IOException | Yanlış şifre veya bozuk dosya varsa atılır. |
| SecurityException | Belirtilen takma adda özel anahtar yoksa atılır |

## Örnekler

SertifikaHolder nesnelerinin nasıl oluşturulacağını gösterir.

```csharp
// Aşağıda SertifikaHolder nesneleri oluşturmanın dört yolu verilmiştir.
// 1 - Bir PKCS #12 dosyasını bayt dizisine yükleyin ve şifresini uygulayın:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Bir bayt dizisine PKCS #12 dosyasını yükleyin ve güvenli bir parola uygulayın:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Sertifikanın takma adlara karşılık gelen özel anahtarları varsa,
// ilgili anahtarları almak için takma adları kullanabiliriz. Öncelikle geçerli takma adları kontrol edeceğiz.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12StoreBuilder().Build();
    pkcs12Store.Load(certStream, "aw".ToCharArray());
    IEnumerator enumerator = pkcs12Store.Aliases.GetEnumerator();

    while (enumerator.MoveNext())
    {
        if (enumerator.Current != null)
        {
            string currentAlias = enumerator.Current.ToString();
            if (pkcs12Store.IsKeyEntry(currentAlias) && pkcs12Store.GetKey(currentAlias).Key.IsPrivate)
            {
                Console.WriteLine($"Valid alias found: {enumerator.Current}");
            }
        }
    }
}

// 3 - Geçerli bir takma ad kullanın:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Özel anahtar döndüren ilk mevcut takma adı kullanmak için takma ad olarak "null"u iletin:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Ayrıca bakınız

* class [CertificateHolder](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)
