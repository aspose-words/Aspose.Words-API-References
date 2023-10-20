---
title: WarningInfoCollection Class
linktitle: WarningInfoCollection
articleTitle: WarningInfoCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.WarningInfoCollection sınıf. Yazılı bir koleksiyonu temsil ederWarningInfo nesneler C#'da.
type: docs
weight: 6640
url: /tr/net/aspose.words/warninginfocollection/
---
## WarningInfoCollection class

Yazılı bir koleksiyonu temsil eder[`WarningInfo`](../warninginfo/) nesneler.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Belgelerle Programlama](https://docs.aspose.com/words/net/programming-with-documents/) dokümantasyon makalesi.

```csharp
public class WarningInfoCollection : IEnumerable<WarningInfo>, IWarningCallback
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [WarningInfoCollection](warninginfocollection/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/warninginfocollection/count/) { get; } | Koleksiyonda yer alan öğelerin sayısını alır. |
| [Item](../../aspose.words/warninginfocollection/item/) { get; } | Belirtilen dizindeki bir öğeyi alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clear](../../aspose.words/warninginfocollection/clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [GetEnumerator](../../aspose.words/warninginfocollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir numaralandırıcı nesnesini döndürür. |
| [Warning](../../aspose.words/warninginfocollection/warning/)(*[WarningInfo](../warninginfo/)*) | Uygular[`IWarningCallback`](../iwarningcallback/) arayüz. Bu koleksiyona bir uyarı ekler. |

## Notlar

Bu koleksiyon nesnesini en basit biçimi olarak kullanabilirsiniz.[`IWarningCallback`](../iwarningcallback/) Aspose.Words'ün yükleme veya kaydetme işlemi sırasında ürettiği tüm uyarıları toplamak için uygulama. Bu sınıfın bir örneğini oluşturun ve onu olarak atayın.[`WarningCallback`](../../aspose.words.loading/loadoptions/warningcallback/) veya[`WarningCallback`](../documentbase/warningcallback/) mülk.

## Örnekler

Mevcut yazı tipi kaynaklarından eksik bir yazı tipi için en yakın eşleşmeyi bulma özelliğinin nasıl ayarlanacağını gösterir.

```csharp
public void EnableFontSubstitution()
{
    // Yazı tipi kaynaklarımızın hiçbirinde bulunmayan bir yazı tipiyle biçimlendirilmiş metni içeren bir belge açın.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Yazı tipi değiştirme uyarılarını işlemek için bir geri arama atayın.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Varsayılan bir yazı tipi adı belirleyin ve yazı tipi değiştirmeyi etkinleştirin.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // Font değişiminden sonra orijinal font metrikleri kullanılmalıdır.
    doc.LayoutOptions.KeepOriginalFontMetrics = true;

    // Fontu eksik olan bir belgeyi kaydedersek font değiştirme uyarısı alacağız.
    doc.FontSettings = fontSettings;
    doc.Save(ArtifactsDir + "FontSettings.EnableFontSubstitution.pdf");

    using (IEnumerator<WarningInfo> warnings = substitutionWarningHandler.FontWarnings.GetEnumerator())
        while (warnings.MoveNext())
            Console.WriteLine(warnings.Current.Description);

    // Koleksiyondaki uyarıları da doğrulayıp temizleyebiliriz.
    Assert.AreEqual(WarningSource.Layout, substitutionWarningHandler.FontWarnings[0].Source);
    Assert.AreEqual(
        "Font '28 Days Later' has not been found. Using 'Calibri' font instead. Reason: alternative name from document.",
        substitutionWarningHandler.FontWarnings[0].Description);

    substitutionWarningHandler.FontWarnings.Clear();

    Assert.That(substitutionWarningHandler.FontWarnings, Is.Empty);
}

public class HandleDocumentSubstitutionWarnings : IWarningCallback
{
    /// <summary>
    /// Yükleme/kaydetme sırasında her uyarı oluştuğunda çağrılır.
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

* class [WarningInfo](../warninginfo/)
* interface [IWarningCallback](../iwarningcallback/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
