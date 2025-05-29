---
title: License.SetLicense
linktitle: SetLicense
articleTitle: SetLicense
second_title: .NET için Aspose.Words
description: SetLicense yöntemimizle bileşenlerinizi zahmetsizce lisanslayın. Tam işlevselliğin kilidini açın ve projenizin potansiyelini bugün artırın!
type: docs
weight: 20
url: /tr/net/aspose.words/license/setlicense/
---
## SetLicense(*string*) {#setlicense_1}

Bileşeni lisanslar.

```csharp
public void SetLicense(string licenseName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| licenseName | String | Tam veya kısa dosya adı veya gömülü bir kaynağın adı olabilir. Değerlendirme moduna geçmek için boş bir dize kullanın. |

## Notlar

Aşağıdaki konumlarda lisansı bulmaya çalışır:

1. Açık yol.

2. Aspose bileşen derlemesini içeren klasör.

3. İstemcinin çağıran derlemesini içeren klasör.

4. Giriş (başlangıç) derlemesini içeren klasör.

5. İstemcinin çağıran derlemesinde gömülü bir kaynak.

**Not:**.NET Compact Framework'te, lisansı yalnızca şu konumlarda bulmaya çalışır:

1. Açık yol.

2. İstemcinin çağıran derlemesinde gömülü bir kaynak.

## Örnekler

Yerel dosya sistemindeki bir lisans dosyasını kullanarak Aspose.Words için bir lisansın nasıl başlatılacağını gösterir.

```csharp
// Aspose.Words ürünümüz için geçerli bir lisans dosyasının yerel dosya sistemi dosya adını geçirerek lisansı ayarlayın.
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// Uygulamamızın binaries klasöründe lisans dosyamızın bir kopyasını oluşturalım.
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// Eğer bir dosyanın adını yol olmadan geçirirsek,
// SetLicense bu dosyayı çeşitli yerel dosya sistemi konumlarında arayacaktır.
// Bu konumlardan biri, lisans dosyamızın bir kopyasını içeren "bin" klasörü olacaktır.
license.SetLicense("Aspose.Words.NET.lic");
```

### Ayrıca bakınız

* class [License](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## SetLicense(*Stream*) {#setlicense}

Bileşeni lisanslar.

```csharp
public void SetLicense(Stream stream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Lisansı içeren bir akış. |

## Notlar

Bir akıştan lisans yüklemek için bu yöntemi kullanın.

## Örnekler

Bir akıştan Aspose.Words için bir lisansın nasıl başlatılacağını gösterir.

```csharp
// Yerel dosya sistemimizdeki geçerli bir lisans dosyası için bir akış geçirerek Aspose.Words ürünümüz için lisansı ayarlayın.
using (Stream myStream = File.OpenRead(Path.Combine(LicenseDir, "Aspose.Words.NET.lic")))
{
    License license = new License();
    license.SetLicense(myStream);
}
```

### Ayrıca bakınız

* class [License](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
