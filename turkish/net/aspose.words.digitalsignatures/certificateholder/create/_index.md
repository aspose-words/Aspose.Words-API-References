---
title: Create
second_title: Aspose.Words for .NET API Referansı
description: PKCS12 deposunun bayt dizisini ve parolasını kullanarak CertificateHolder nesnesi oluşturur.
type: docs
weight: 10
url: /tr/net/aspose.words.digitalsignatures/certificateholder/create/
---
## Create(byte[], SecureString) {#create}

PKCS12 deposunun bayt dizisini ve parolasını kullanarak CertificateHolder nesnesi oluşturur.

```csharp
public static CertificateHolder Create(byte[] certBytes, SecureString password)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| certBytes | Byte[] | X.509 sertifikasındaki verileri içeren bir bayt dizisi. |
| password | SecureString | X.509 sertifika verilerine erişmek için gereken parola. |

### Geri dönüş değeri

CertificateHolder örneği

### istisnalar

| istisna | şart |
| --- | --- |
| InvalidParameterException | atılırsa **certBytes** boş |
| InvalidParameterException | atılırsa **şifre** boş |
| SecurityException | PKCS12 deposu takma ad içermiyorsa atılır |
| IOException | Yanlış şifre veya bozuk dosya varsa atılır. |

### Örnekler

CertificateHolder nesnelerinin nasıl oluşturulacağını gösterir.

```csharp
// Aşağıda, CertificateHolder nesneleri oluşturmanın dört yolu bulunmaktadır.
// 1 - Bir bayt dizisine bir PKCS #12 dosyası yükleyin ve şifresini uygulayın:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Bir bayt dizisine bir PKCS #12 dosyası yükleyin ve güvenli bir parola uygulayın:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Sertifikanın takma adlara karşılık gelen özel anahtarları varsa,
// ilgili anahtarları almak için takma adları kullanabiliriz. İlk olarak, geçerli takma adları kontrol edeceğiz.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12Store(certStream, "aw".ToCharArray());
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

// 4 - Özel anahtar döndüren ilk kullanılabilir diğer adı kullanmak için takma ad olarak "null" değerini iletin:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Ayrıca bakınız

* class [CertificateHolder](../../certificateholder)
* ad alanı [Aspose.Words.DigitalSignatures](../../certificateholder)
* toplantı [Aspose.Words](../../../)

---

## Create(byte[], string) {#create_1}

PKCS12 deposunun bayt dizisini ve parolasını kullanarak CertificateHolder nesnesi oluşturur.

```csharp
public static CertificateHolder Create(byte[] certBytes, string password)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| certBytes | Byte[] | X.509 sertifikasındaki verileri içeren bir bayt dizisi. |
| password | String | X.509 sertifika verilerine erişmek için gereken parola. |

### Geri dönüş değeri

CertificateHolder örneği

### istisnalar

| istisna | şart |
| --- | --- |
| InvalidParameterException | atılırsa **certBytes** boş |
| InvalidParameterException | atılırsa **şifre** boş |
| SecurityException | PKCS12 deposu takma ad içermiyorsa atılır |
| IOException | Yanlış şifre veya bozuk dosya varsa atılır. |

### Örnekler

CertificateHolder nesnelerinin nasıl oluşturulacağını gösterir.

```csharp
// Aşağıda, CertificateHolder nesneleri oluşturmanın dört yolu bulunmaktadır.
// 1 - Bir bayt dizisine bir PKCS #12 dosyası yükleyin ve şifresini uygulayın:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Bir bayt dizisine bir PKCS #12 dosyası yükleyin ve güvenli bir parola uygulayın:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Sertifikanın takma adlara karşılık gelen özel anahtarları varsa,
// ilgili anahtarları almak için takma adları kullanabiliriz. İlk olarak, geçerli takma adları kontrol edeceğiz.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12Store(certStream, "aw".ToCharArray());
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

// 4 - Özel anahtar döndüren ilk kullanılabilir diğer adı kullanmak için takma ad olarak "null" değerini iletin:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Ayrıca bakınız

* class [CertificateHolder](../../certificateholder)
* ad alanı [Aspose.Words.DigitalSignatures](../../certificateholder)
* toplantı [Aspose.Words](../../../)

---

## Create(string, string) {#create_2}

PKCS12 deposunun yolunu ve parolasını kullanarak CertificateHolder nesnesi oluşturur.

```csharp
public static CertificateHolder Create(string fileName, string password)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Bir sertifika dosyasının adı. |
| password | String | X.509 sertifika verilerine erişmek için gereken parola. |

### Geri dönüş değeri

CertificateHolder örneği

### istisnalar

| istisna | şart |
| --- | --- |
| InvalidParameterException | atılırsa **dosya adı** boş |
| InvalidParameterException | atılırsa **şifre** boş |
| SecurityException | PKCS12 deposu takma ad içermiyorsa atılır |
| IOException | Yanlış şifre veya bozuk dosya varsa atılır. |

### Örnekler

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

// Dosya akışı yoluyla yerel dosya sisteminden imzasız bir belge alın,
// ardından çıktı dosyası akışının dosya adıyla belirlenen imzalı bir kopyasını oluşturun.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Ayrıca bakınız

* class [CertificateHolder](../../certificateholder)
* ad alanı [Aspose.Words.DigitalSignatures](../../certificateholder)
* toplantı [Aspose.Words](../../../)

---

## Create(string, string, string) {#create_3}

PKCS12 deposunun yolunu, parolasını ve diğer adı kullanarak, hangi özel anahtar ve sertifikanın bulunacağını kullanarak CertificateHolder nesnesi oluşturur.

```csharp
public static CertificateHolder Create(string fileName, string password, string alias)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Bir sertifika dosyasının adı. |
| password | String | X.509 sertifika verilerine erişmek için gereken parola. |
| alias | String | Bir sertifika ve özel anahtarı için ilişkili diğer ad |

### Geri dönüş değeri

CertificateHolder örneği

### istisnalar

| istisna | şart |
| --- | --- |
| InvalidParameterException | atılırsa **dosya adı** boş |
| InvalidParameterException | atılırsa **şifre** boş |
| SecurityException | PKCS12 deposu takma ad içermiyorsa atılır |
| IOException | Yanlış şifre veya bozuk dosya varsa atılır. |
| SecurityException | Verilen takma adla özel anahtar yoksa atılır |

### Örnekler

CertificateHolder nesnelerinin nasıl oluşturulacağını gösterir.

```csharp
// Aşağıda, CertificateHolder nesneleri oluşturmanın dört yolu bulunmaktadır.
// 1 - Bir bayt dizisine bir PKCS #12 dosyası yükleyin ve şifresini uygulayın:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Bir bayt dizisine bir PKCS #12 dosyası yükleyin ve güvenli bir parola uygulayın:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Sertifikanın takma adlara karşılık gelen özel anahtarları varsa,
// ilgili anahtarları almak için takma adları kullanabiliriz. İlk olarak, geçerli takma adları kontrol edeceğiz.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12Store(certStream, "aw".ToCharArray());
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

// 4 - Özel anahtar döndüren ilk kullanılabilir diğer adı kullanmak için takma ad olarak "null" değerini iletin:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Ayrıca bakınız

* class [CertificateHolder](../../certificateholder)
* ad alanı [Aspose.Words.DigitalSignatures](../../certificateholder)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
