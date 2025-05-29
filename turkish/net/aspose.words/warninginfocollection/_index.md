---
title: WarningInfoCollection Class
linktitle: WarningInfoCollection
articleTitle: WarningInfoCollection
second_title: .NET için Aspose.Words
description: WarningInfo nesnelerini yönetmek, belge işlemeyi ve hata işlemeyi geliştirmek için güçlü bir sınıf olan Aspose.Words.WarningInfoCollection'ı keşfedin.
type: docs
weight: 7490
url: /tr/net/aspose.words/warninginfocollection/
---
## WarningInfoCollection class

Türlü bir koleksiyonu temsil eder[`WarningInfo`](../warninginfo/) nesneler.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Belgelerle Programlama](https://docs.aspose.com/words/net/programming-with-documents/) belgeleme makalesi.

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
| [Count](../../aspose.words/warninginfocollection/count/) { get; } | Koleksiyonda bulunan öğelerin sayısını alır. |
| [Item](../../aspose.words/warninginfocollection/item/) { get; } | Belirtilen dizindeki bir öğeyi alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clear](../../aspose.words/warninginfocollection/clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [GetEnumerator](../../aspose.words/warninginfocollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilen bir numaratör nesnesi döndürür. |
| [Warning](../../aspose.words/warninginfocollection/warning/)(*[WarningInfo](../warninginfo/)*) | Şunu uygular:[`IWarningCallback`](../iwarningcallback/) arayüz. Bu koleksiyona bir uyarı ekler. |

## Notlar

Bu koleksiyon nesnesini en basit haliyle kullanabilirsiniz[`IWarningCallback`](../iwarningcallback/) Aspose.Words'ün bir yükleme veya kaydetme işlemi sırasında ürettiği tüm uyarıları toplamak için uygulaması. Bu sınıfın bir örneğini oluşturun ve bunu 'ye atayın[`WarningCallback`](../../aspose.words.loading/loadoptions/warningcallback/) veya[`WarningCallback`](../documentbase/warningcallback/) mülk.

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

* class [WarningInfo](../warninginfo/)
* interface [IWarningCallback](../iwarningcallback/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
