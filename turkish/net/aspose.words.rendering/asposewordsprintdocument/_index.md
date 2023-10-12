---
title: Class AsposeWordsPrintDocument
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Rendering.AsposeWordsPrintDocument sınıf. Bir belgenin yazdırılması için varsayılan bir uygulama sağlar.Document .NET yazdırma çerçevesi dahilinde .
type: docs
weight: 4530
url: /tr/net/aspose.words.rendering/asposewordsprintdocument/
---
## AsposeWordsPrintDocument class

Bir belgenin yazdırılması için varsayılan bir uygulama sağlar.[`Document`](../../aspose.words/document/) .NET yazdırma çerçevesi dahilinde .

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Bir Belgeyi Programlı Olarak Yazdırma veya İletişim Kutularını Kullanma](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) dokümantasyon makalesi.

```csharp
public class AsposeWordsPrintDocument : PrintDocument
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [AsposeWordsPrintDocument](asposewordsprintdocument/)(Document) | Bu sınıfın yeni bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ColorMode](../../aspose.words.rendering/asposewordsprintdocument/colormode/) { get; set; } | Aygıt renkli yazdırmayı destekliyorsa, renkli olmayan sayfaların nasıl yazdırılacağını alır veya ayarlar. |
| [ColorPagesPrinted](../../aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/) { get; } | Renkli olarak yazdırılan sayfa sayısını alır (ör.Color true olarak ayarlandı). |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [CachePrinterSettings](../../aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/)() | Bazı alanları okur ve önbelleğe alırPrinterSettings yazdırma süresini azaltmak için. |

### Notlar

`AsposeWordsPrintDocument` geçersiz kılmalarPrintEventArgs) belirtilen sayfa aralığını yazdırmak içinPrinterSettings.

Tek bir Word belgesi, farklı boyutlara, yönlendirmeye ve kağıt tepsilerine sahip sayfaları belirten birden çok bölümden oluşabilir.`AsposeWordsPrintDocument` geçersiz kılmalar QueryPageSettingsEventArgs) Bir Word belgesini yazdırırken kağıt boyutunu, yönlendirme 'yi ve kağıt kaynağını doğru şekilde seçmek için.

Microsoft Word, kağıt tepsileri için yazıcıya özgü değerleri bir Word belgesinde saklar ve bu nedenle, yalnızca kullanıcı kağıt tepsileri 'yi belirttiğinde seçilen yazıcı modeliyle aynı yazıcı modelinde yazdırma, doğru tepsilerden yazdırmayla sonuçlanacaktır. Bir belgeyi farklı bir yazıcıda yazdırırsanız, büyük olasılıkla belgede belirtilen tepsiler değil, varsayılan kağıt tepsisi kullanılacaktır.

### Ayrıca bakınız

* ad alanı [Aspose.Words.Rendering](../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../)


