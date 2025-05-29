---
title: PageSetup.OtherPagesTray
linktitle: OtherPagesTray
articleTitle: OtherPagesTray
second_title: .NET için Aspose.Words
description: Yazıcınız için kağıt tepsisi ayarlarını kolayca özelleştirmek için PageSetup OtherPagesTray özelliğini keşfedin. Her bölüm için yazdırma verimliliğini optimize edin!
type: docs
weight: 300
url: /tr/net/aspose.words/pagesetup/otherpagestray/
---
## PageSetup.OtherPagesTray property

Bir bölümün ilk sayfası hariç tüm sayfaları için kullanılacak kağıt tepsisini (kutu) alır veya ayarlar. Değer, uygulamaya (yazıcıya) özgüdür.

```csharp
public int OtherPagesTray { get; set; }
```

## Örnekler

Seçili yazıcının varsayılan kağıt tepsisinin bir belgedeki tüm bölümleri nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();

// Bu belgeyi yazdırmak için kullanacağımız varsayılan yazıcıyı bulalım.
// PrinterSettings nesnesinin "PrinterName" özelliğini kullanarak belirli bir yazıcı tanımlayabilirsiniz.
PrinterSettings settings = new PrinterSettings();

// Belgelerde saklanan kağıt tepsisi değeri yazıcıya özgüdür.
// Bu, aşağıdaki kodun tüm sayfa tepsisi değerlerini, geçerli yazıcının varsayılan tepsisini kullanacak şekilde sıfırladığı anlamına gelir.
// Seçili yazıcının diğer geçerli kağıt tepsisi değerlerini bulmak için PrinterSettings.PaperSources'ı numaralandırabilirsiniz.
foreach (Section section in doc.Sections.OfType<Section>())
{
    section.PageSetup.FirstPageTray = settings.DefaultPageSettings.PaperSource.RawKind;
    section.PageSetup.OtherPagesTray = settings.DefaultPageSettings.PaperSource.RawKind;
}
```

Farklı kağıt boyutları için farklı yazıcı tepsileri kullanılarak yazdırmanın nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();

// Bu belgeyi yazdırmak için kullanacağımız varsayılan yazıcıyı bulalım.
// PrinterSettings nesnesinin "PrinterName" özelliğini kullanarak belirli bir yazıcı tanımlayabilirsiniz.
PrinterSettings settings = new PrinterSettings();

// Bu, "A4" kağıt boyutundaki sayfalar için kullanacağımız tepsidir.
int printerTrayForA4 = settings.PaperSources[0].RawKind;

// Bu, "Letter" kağıt boyutundaki sayfalar için kullanacağımız tepsidir.
int printerTrayForLetter = settings.PaperSources[1].RawKind;

// Microsoft Word'ün yazıcıya talimat vermesini sağlamak için bu bölümün PageSettings nesnesini değiştirin
// Bu bölümün kağıt boyutuna bağlı olarak yukarıda tanımladığımız tepsilerden birini kullanmak için.
foreach (Section section in doc.Sections.OfType<Section>())
{
    if (section.PageSetup.PaperSize == Aspose.Words.PaperSize.Letter)
    {
        section.PageSetup.FirstPageTray = printerTrayForLetter;
        section.PageSetup.OtherPagesTray = printerTrayForLetter;
    }
    else if (section.PageSetup.PaperSize == Aspose.Words.PaperSize.A4)
    {
        section.PageSetup.FirstPageTray = printerTrayForA4;
        section.PageSetup.OtherPagesTray = printerTrayForA4;
    }
}
```

### Ayrıca bakınız

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
