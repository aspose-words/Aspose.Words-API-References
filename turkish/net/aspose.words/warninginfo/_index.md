---
title: WarningInfo Class
linktitle: WarningInfo
articleTitle: WarningInfo
second_title: .NET için Aspose.Words
description: Belge yükleme veya kaydetme sırasında uyarılar hakkında önemli bilgiler sağlayan ve iş akışı verimliliğinizi artıran Aspose.Words.WarningInfo sınıfını keşfedin.
type: docs
weight: 7480
url: /tr/net/aspose.words/warninginfo/
---
## WarningInfo class

Aspose.Words'ün belge yükleme veya kaydetme sırasında verdiği bir uyarı hakkında bilgi içerir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Belgelerle Programlama](https://docs.aspose.com/words/net/programming-with-documents/) belgeleme makalesi.

```csharp
public class WarningInfo
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Description](../../aspose.words/warninginfo/description/) { get; } | Uyarının açıklamasını döndürür. |
| [Source](../../aspose.words/warninginfo/source/) { get; } | Uyarının kaynağını döndürür. |
| [WarningType](../../aspose.words/warninginfo/warningtype/) { get; } | Uyarının türünü döndürür. |

## Notlar

Bu sınıfın örneklerini oluşturmazsınız. Bu sınıfın nesneleri created olur ve Aspose.Words tarafından[`Warning`](../iwarningcallback/warning/) yöntem.

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
