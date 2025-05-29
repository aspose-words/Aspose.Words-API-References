---
title: WarningType Enum
linktitle: WarningType
articleTitle: WarningType
second_title: .NET için Aspose.Words
description: Belge yükleme veya kaydetme sırasında uyarıları kategorilere ayıran ve belge yönetimi deneyiminizi geliştiren Aspose.Words.WarningType enum'ını keşfedin.
type: docs
weight: 7510
url: /tr/net/aspose.words/warningtype/
---
## WarningType enumeration

Belge yükleme veya kaydetme sırasında Aspose.Words tarafından verilen uyarının türünü belirtir.

```csharp
[Flags]
public enum WarningType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| DataLossCategory | `FF` | Yüklemeden sonra belge ağacında bazı metin/karakter/görüntü veya diğer veriler kaybolacaktır, veya kaydetmeden sonra oluşturulan belgede. |
| DataLoss | `1` | Genel veri kaybı, belirli bir kod yok. |
| MajorFormattingLossCategory | `FF00` | Ortaya çıkan belge veya içindeki belirli bir konum, orijinal belgeye kıyasla önemli ölçüde farklı görünebilir. |
| MajorFormattingLoss | `100` | Genel büyük biçimlendirme kaybı, belirli bir kod yok. |
| MinorFormattingLossCategory | `FF0000` | Ortaya çıkan belge veya içindeki belirli bir konum, orijinal belgeye kıyasla biraz farklı görünebilir. |
| MinorFormattingLoss | `10000` | Genel küçük biçimlendirme kaybı, belirli bir kod yok. |
| FontSubstitution | `20000` | Yazı tipi değiştirildi. |
| FontEmbedding | `40000` | Belge kaydedilirken gömülü yazı tipi bilgilerinin kaybı. |
| UnexpectedContentCategory | `F000000` | Kaynak belgedeki bazı içerikler tanınamadı (yani desteklenmiyor), bu sorunlara yol açabilir veya açmayabilir veya veri/biçimlendirme kaybına neden olabilir. |
| UnexpectedContent | `1000000` | Genel beklenmeyen içerik, belirli bir kod yok. |
| Hint | `10000000` | Olası bir sorunu bildirir veya bir iyileştirme önerir. |

## Örnekler

Mevcut yazı tipi kaynaklarından eksik bir yazı tipi için en yakın eşleşmeyi bulma özelliğinin nasıl ayarlanacağını gösterir.

```csharp
public void EnableFontSubstitution()
{
    // Yazı tipi kaynaklarımızın hiçbirinde bulunmayan bir yazı tipiyle biçimlendirilmiş metin içeren bir belgeyi açın.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Yazı tipi değiştirme uyarılarını işlemek için bir geri çağırma atayın.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Varsayılan bir yazı tipi adı belirleyin ve yazı tipi değişimini etkinleştirin.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // Font değişiminden sonra orijinal font ölçütleri kullanılmalıdır.
    doc.LayoutOptions.KeepOriginalFontMetrics = true;

    // Eksik font içeren bir belgeyi kaydedersek font değiştirme uyarısı alırız.
    doc.FontSettings = fontSettings;
    doc.Save(ArtifactsDir + "FontSettings.EnableFontSubstitution.pdf");

    using (IEnumerator<WarningInfo> warnings = substitutionWarningHandler.FontWarnings.GetEnumerator())
        while (warnings.MoveNext())
            Console.WriteLine(warnings.Current.Description);

    // Ayrıca koleksiyondaki uyarıları doğrulayabilir ve temizleyebiliriz.
    Assert.AreEqual(WarningSource.Layout, substitutionWarningHandler.FontWarnings[0].Source);
    Assert.AreEqual(
        "Font '28 Days Later' has not been found. Using 'Calibri' font instead. Reason: alternative name from document.",
        substitutionWarningHandler.FontWarnings[0].Description);

    substitutionWarningHandler.FontWarnings.Clear();

    Assert.AreEqual(0, substitutionWarningHandler.FontWarnings.Count);
}

public class HandleDocumentSubstitutionWarnings : IWarningCallback
{
    /// <summary>
    /// Yükleme/kaydetme sırasında bir uyarı oluştuğunda her seferinde çağrılır.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontWarnings.Warning(info);
    }

    public WarningInfoCollection FontWarnings = new WarningInfoCollection();
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
