---
title: License.SetLicense
second_title: Aspose.Words for .NET API Referansı
description: License yöntem. Bileşeni lisanslar.
type: docs
weight: 20
url: /tr/net/aspose.words/license/setlicense/
---
## SetLicense(string) {#setlicense_1}

Bileşeni lisanslar.

```csharp
public void SetLicense(string licenseName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| licenseName | String | Tam veya kısa dosya adı veya gömülü kaynağın adı olabilir. Değerlendirme moduna geçmek için boş bir dize kullanın. |

### Notlar

Lisansı aşağıdaki konumlarda bulmaya çalışır:

1. Açık yol.

2. Aspose bileşen montajını içeren klasör.

3. İstemcinin çağıran derlemesini içeren klasör.

4. Giriş (başlangıç) derlemesini içeren klasör.

5. İstemcinin çağıran derlemesinde yerleşik bir kaynak.

**Not:**.NET Compact Framework'te lisansı yalnızca şu konumlarda bulmaya çalışır:

1. Açık yol.

2. İstemcinin çağıran derlemesindeki yerleşik bir kaynak.

### Örnekler

Yerel dosya sistemindeki bir lisans dosyasını kullanarak Aspose.Words lisansının nasıl başlatıldığını gösterir.

```csharp
// Geçerli bir lisans dosyasının yerel dosya sistemi dosya adını ileterek Aspose.Words ürünümüzün lisansını ayarlayın.
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// Uygulamamızın ikili dosyalar klasöründe lisans dosyamızın bir kopyasını oluşturun.
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// Bir dosyanın adını yol olmadan aktarırsak,
// SetLicense bu dosya için çeşitli yerel dosya sistemi konumlarını arayacaktır.
// Bu konumlardan biri lisans dosyamızın bir kopyasını içeren "bin" klasörü olacaktır.
license.SetLicense("Aspose.Words.NET.lic");
```

### Ayrıca bakınız

* class [License](../)
* ad alanı [Aspose.Words](../../license/)
* toplantı [Aspose.Words](../../../)

---

## SetLicense(Stream) {#setlicense}

Bileşeni lisanslar.

```csharp
public void SetLicense(Stream stream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Lisansı içeren bir akış. |

### Notlar

Bir akıştan lisans yüklemek için bu yöntemi kullanın.

### Örnekler

Aspose.Words lisansının bir akıştan nasıl başlatılacağını gösterir.

```csharp
// Yerel dosya sistemimizde geçerli bir lisans dosyası için bir akış ileterek Aspose.Words ürünümüzün lisansını ayarlayın.
using (Stream myStream = File.OpenRead(Path.Combine(LicenseDir, "Aspose.Words.NET.lic")))
{
    License license = new License();
    license.SetLicense(myStream);
}
```

### Ayrıca bakınız

* class [License](../)
* ad alanı [Aspose.Words](../../license/)
* toplantı [Aspose.Words](../../../)


