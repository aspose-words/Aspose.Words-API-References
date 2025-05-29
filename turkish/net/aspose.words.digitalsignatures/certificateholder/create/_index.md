---
title: CertificateHolder.Create
linktitle: Create
articleTitle: Create
second_title: .NET için Aspose.Words
description: PKCS12 bayt dizisinden ve paroladan zahmetsizce bir CertificateHolder nesnesi oluşturun. Sezgisel yöntemimizle sertifika yönetimini basitleştirin.
type: docs
weight: 10
url: /tr/net/aspose.words.digitalsignatures/certificateholder/create/
---
## Create(*byte[], SecureString*) {#create}

Oluşturur[`CertificateHolder`](../) PKCS12 deposunun bayt dizisini ve şifresini kullanan nesne.

```csharp
public static CertificateHolder Create(byte[] certBytes, SecureString password)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| certBytes | Byte[] | X.509 sertifikasından veri içeren bir bayt dizisi. |
| password | SecureString | X.509 sertifika verilerine erişmek için gereken şifre. |

### Geri dönüş değeri

Bir örneği[`CertificateHolder`](../)

### istisnalar

| istisna | şart |
| --- | --- |
| InvalidParameterException | Eğer atılmışsa*certBytes* dır`hükümsüz` |
| InvalidParameterException | Eğer atılmışsa*password* dır`hükümsüz` |
| SecurityException | PKCS12 deposunda takma ad yoksa atılır |
| IOException | Yanlış şifre veya bozuk dosya olması durumunda atılır. |

## Örnekler

CertificateHolder nesnelerinin nasıl oluşturulacağını gösterir.

```csharp
// Aşağıda CertificateHolder nesnelerini oluşturmanın dört yolu bulunmaktadır.
// 1 - Bir PKCS #12 dosyasını bir bayt dizisine yükleyin ve şifresini uygulayın:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Bir PKCS #12 dosyasını bir bayt dizisine yükleyin ve güvenli bir parola uygulayın:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Sertifikanın takma adlara karşılık gelen özel anahtarları varsa,
// ilgili anahtarlarını almak için takma adları kullanabiliriz. İlk olarak geçerli takma adları kontrol edeceğiz.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12StoreBuilder().Build();
    pkcs12Store.Load(certStream, "aw".ToCharArray());
    foreach (string currentAlias in pkcs12Store.Aliases)
    {
        if ((currentAlias != null) &&
            (pkcs12Store.IsKeyEntry(currentAlias) &&
             pkcs12Store.GetKey(currentAlias).Key.IsPrivate))
        {
            Console.WriteLine($"Valid alias found: {currentAlias}");
        }
    }
}

// 3 - Geçerli bir takma ad kullanın:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Özel bir anahtar döndüren ilk kullanılabilir takma adı kullanmak için takma ad olarak "null" değerini geçirin:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Ayrıca bakınız

* class [CertificateHolder](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)

---

## Create(*byte[], string*) {#create_1}

Oluşturur[`CertificateHolder`](../) PKCS12 deposunun bayt dizisini ve şifresini kullanan nesne.

```csharp
public static CertificateHolder Create(byte[] certBytes, string password)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| certBytes | Byte[] | X.509 sertifikasından veri içeren bir bayt dizisi. |
| password | String | X.509 sertifika verilerine erişmek için gereken şifre. |

### Geri dönüş değeri

Bir örneği[`CertificateHolder`](../)

### istisnalar

| istisna | şart |
| --- | --- |
| InvalidParameterException | Eğer atılmışsa*certBytes* dır`hükümsüz` |
| InvalidParameterException | Eğer atılmışsa*password* dır`hükümsüz` |
| SecurityException | PKCS12 deposunda takma ad yoksa atılır |
| IOException | Yanlış şifre veya bozuk dosya olması durumunda atılır. |

## Örnekler

CertificateHolder nesnelerinin nasıl oluşturulacağını gösterir.

```csharp
// Aşağıda CertificateHolder nesnelerini oluşturmanın dört yolu bulunmaktadır.
// 1 - Bir PKCS #12 dosyasını bir bayt dizisine yükleyin ve şifresini uygulayın:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Bir PKCS #12 dosyasını bir bayt dizisine yükleyin ve güvenli bir parola uygulayın:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Sertifikanın takma adlara karşılık gelen özel anahtarları varsa,
// ilgili anahtarlarını almak için takma adları kullanabiliriz. İlk olarak geçerli takma adları kontrol edeceğiz.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12StoreBuilder().Build();
    pkcs12Store.Load(certStream, "aw".ToCharArray());
    foreach (string currentAlias in pkcs12Store.Aliases)
    {
        if ((currentAlias != null) &&
            (pkcs12Store.IsKeyEntry(currentAlias) &&
             pkcs12Store.GetKey(currentAlias).Key.IsPrivate))
        {
            Console.WriteLine($"Valid alias found: {currentAlias}");
        }
    }
}

// 3 - Geçerli bir takma ad kullanın:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Özel bir anahtar döndüren ilk kullanılabilir takma adı kullanmak için takma ad olarak "null" değerini geçirin:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Ayrıca bakınız

* class [CertificateHolder](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)

---

## Create(*string, string*) {#create_2}

Oluşturur[`CertificateHolder`](../)PKCS12 deposuna giden yolu ve parolasını kullanan nesne.

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
| InvalidParameterException | Eğer atılmışsa*fileName* dır`hükümsüz` |
| InvalidParameterException | Eğer atılmışsa*password* dır`hükümsüz` |
| SecurityException | PKCS12 deposunda takma ad yoksa atılır |
| IOException | Yanlış şifre veya bozuk dosya olması durumunda atılır. |

## Örnekler

Belgelerin dijital olarak nasıl imzalanacağını gösterir.

```csharp
// Özel bir anahtar içermesi gereken bir PKCS#12 deposundan bir X.509 sertifikası oluşturun.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Yeni dijital imzamızla uygulanacak bir yorum ve tarih oluşturun.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Yerel dosya sisteminden bir dosya akışı aracılığıyla imzalanmamış bir belge alın,
// daha sonra çıktı dosya akışının dosya adına göre belirlenen imzalı bir kopyasını oluşturur.
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

Oluşturur[`CertificateHolder`](../) PKCS12 deposuna giden yolu, parolasını ve özel anahtar ve sertifikanın bulunacağı takma adı kullanan nesne.

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
| InvalidParameterException | Eğer atılmışsa*fileName* dır`hükümsüz` |
| InvalidParameterException | Eğer atılmışsa*password* dır`hükümsüz` |
| SecurityException | PKCS12 deposunda takma ad yoksa atılır |
| IOException | Yanlış şifre veya bozuk dosya olması durumunda atılır. |
| SecurityException | Belirtilen takma adla özel anahtar yoksa atılır |

## Örnekler

CertificateHolder nesnelerinin nasıl oluşturulacağını gösterir.

```csharp
// Aşağıda CertificateHolder nesnelerini oluşturmanın dört yolu bulunmaktadır.
// 1 - Bir PKCS #12 dosyasını bir bayt dizisine yükleyin ve şifresini uygulayın:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Bir PKCS #12 dosyasını bir bayt dizisine yükleyin ve güvenli bir parola uygulayın:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Sertifikanın takma adlara karşılık gelen özel anahtarları varsa,
// ilgili anahtarlarını almak için takma adları kullanabiliriz. İlk olarak geçerli takma adları kontrol edeceğiz.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12StoreBuilder().Build();
    pkcs12Store.Load(certStream, "aw".ToCharArray());
    foreach (string currentAlias in pkcs12Store.Aliases)
    {
        if ((currentAlias != null) &&
            (pkcs12Store.IsKeyEntry(currentAlias) &&
             pkcs12Store.GetKey(currentAlias).Key.IsPrivate))
        {
            Console.WriteLine($"Valid alias found: {currentAlias}");
        }
    }
}

// 3 - Geçerli bir takma ad kullanın:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Özel bir anahtar döndüren ilk kullanılabilir takma adı kullanmak için takma ad olarak "null" değerini geçirin:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Ayrıca bakınız

* class [CertificateHolder](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)
