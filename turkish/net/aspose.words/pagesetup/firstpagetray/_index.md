---
title: PageSetup.FirstPageTray
second_title: Aspose.Words for .NET API Referansı
description: PageSetup mülk. Bir bölümün ilk sayfası için kullanılacak kağıt tepsisini bölme alır veya ayarlar. Değer uygulamaya yazıcıya özeldir.
type: docs
weight: 130
url: /tr/net/aspose.words/pagesetup/firstpagetray/
---
## PageSetup.FirstPageTray property

Bir bölümün ilk sayfası için kullanılacak kağıt tepsisini (bölme) alır veya ayarlar. Değer uygulamaya (yazıcıya) özeldir.

```csharp
public int FirstPageTray { get; set; }
```

### Örnekler

Seçilen yazıcının varsayılan kağıt tepsisini kullanmak için bir belgedeki tüm bölümlerin nasıl alınacağını gösterir.

```csharp
Document doc = new Document();

// Bu belgeyi yazdırmak için kullanacağımız varsayılan yazıcıyı bulun.
// PrinterSettings nesnesinin "PrinterName" özelliğini kullanarak belirli bir yazıcı tanımlayabilirsiniz.
PrinterSettings settings = new PrinterSettings();

// Belgelerde saklanan kağıt tepsisi değeri yazıcıya özeldir.
// Bu, aşağıdaki kodun, geçerli yazıcıların varsayılan tepsisini kullanmak için tüm sayfa tepsisi değerlerini sıfırladığı anlamına gelir.
// Seçilen yazıcının diğer geçerli kağıt tepsisi değerlerini bulmak için PrinterSettings.PaperSources'ı numaralandırabilirsiniz.
foreach (Section section in doc.Sections.OfType<Section>())
{
    section.PageSetup.FirstPageTray = settings.DefaultPageSettings.PaperSource.RawKind;
    section.PageSetup.OtherPagesTray = settings.DefaultPageSettings.PaperSource.RawKind;
}
```

Farklı kağıt boyutları için farklı yazıcı tepsilerini kullanarak yazdırmanın nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();

// Bu belgeyi yazdırmak için kullanacağımız varsayılan yazıcıyı bulun.
// PrinterSettings nesnesinin "PrinterName" özelliğini kullanarak belirli bir yazıcı tanımlayabilirsiniz.
PrinterSettings settings = new PrinterSettings();

// "A4" kağıt boyutundaki sayfalar için kullanacağımız tepsi budur.
int printerTrayForA4 = settings.PaperSources[0].RawKind;

// "Mektup" kağıt boyutundaki sayfalar için kullanacağımız tepsi budur.
int printerTrayForLetter = settings.PaperSources[1].RawKind;

// Microsoft Word'ün yazıcıya talimat vermesini sağlamak için bu bölümün PageSettings nesnesini değiştirin
// bu bölümün kağıt boyutuna bağlı olarak yukarıda tanımladığımız tepsilerden birini kullanmak için.
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
* ad alanı [Aspose.Words](../../pagesetup/)
* toplantı [Aspose.Words](../../../)


