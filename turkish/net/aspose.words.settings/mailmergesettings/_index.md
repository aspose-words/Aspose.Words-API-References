---
title: MailMergeSettings Class
linktitle: MailMergeSettings
articleTitle: MailMergeSettings
second_title: .NET için Aspose.Words
description: Gelişmiş verimlilik için güçlü posta birleştirme yetenekleriyle belge otomasyonunu kolaylaştırmak üzere Aspose.Words.MailMergeSettings sınıfını keşfedin.
type: docs
weight: 6680
url: /tr/net/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class

Bir belge için tüm posta birleştirme bilgilerini belirtir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Posta Birleştirme ve Raporlama](https://docs.aspose.com/words/net/mail-merge-and-reporting/) belgeleme makalesi.

```csharp
public class MailMergeSettings
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [MailMergeSettings](mailmergesettings/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ActiveRecord](../../aspose.words.settings/mailmergesettings/activerecord/) { get; set; } | Microsoft Word'de görüntülenecek veri kaynağından gelen kaydın tek tabanlı dizinini belirtir. Varsayılan değer 1'dir. |
| [AddressFieldName](../../aspose.words.settings/mailmergesettings/addressfieldname/) { get; set; } | Veri kaynağında e-posta adreslerini içeren sütunu belirtir. Varsayılan değer boş bir dizedir. |
| [CheckErrors](../../aspose.words.settings/mailmergesettings/checkerrors/) { get; set; } | Microsoft Word tarafından posta birleştirme işlemi gerçekleştirilirken gerçekleştirilecek hata raporlama türünü belirtir. Varsayılan değerDefault . |
| [ConnectString](../../aspose.words.settings/mailmergesettings/connectstring/) { get; set; } | Harici bir veri kaynağına bağlanmak için kullanılan bağlantı dizesini belirtir. Varsayılan değer boş bir dizedir. |
| [DataSource](../../aspose.words.settings/mailmergesettings/datasource/) { get; set; } | Posta birleştirme veri kaynağına giden yolu belirtir. Varsayılan değer boş bir dizedir. |
| [DataType](../../aspose.words.settings/mailmergesettings/datatype/) { get; set; } | Posta birleştirme veri kaynağının türünü ve veri erişim yöntemini belirtir. Varsayılan değer:Default . |
| [Destination](../../aspose.words.settings/mailmergesettings/destination/) { get; set; } | Microsoft Word'ün bir posta birleştirme işleminin sonuçlarını nasıl çıktı vereceğini belirtir. Varsayılan değerDefault . |
| [DoNotSupressBlankLines](../../aspose.words.settings/mailmergesettings/donotsupressblanklines/) { get; set; } | Posta birleştirme işlemini gerçekleştiren bir uygulamanın, posta birleştirme sonucunda birleştirilen belgelerdeki boş satırları nasıl işleyeceğini belirtir. Varsayılan değer:`YANLIŞ` . |
| [HeaderSource](../../aspose.words.settings/mailmergesettings/headersource/) { get; set; } | Posta birleştirme başlık kaynağına giden yolu belirtir. Varsayılan değer boş bir dizedir. |
| [LinkToQuery](../../aspose.words.settings/mailmergesettings/linktoquery/) { get; set; } | Bundan emin değilim. Microsoft Word Otomasyon Başvurusu, bunun sorgunun belgesi Microsoft Word'de her açıldığında yürütüleceğini belirttiğini öne sürüyor. Ancak OOXML belirtimi, bunun sorgunun gerçek sorguyu içeren harici bir sorgu dosyasına bir başvuru içerdiğini belirttiğini öne sürüyor. Varsayılan değer`YANLIŞ` . |
| [MailAsAttachment](../../aspose.words.settings/mailmergesettings/mailasattachment/) { get; set; } | Bir posta birleştirme işlemi sırasında üretilen belgelerin gerçek e-postanın gövdesi yerine eki olarak e-postayla gönderilmesi gerektiğini belirtir. Varsayılan değer`YANLIŞ` . |
| [MailSubject](../../aspose.words.settings/mailmergesettings/mailsubject/) { get; set; } | Posta birleştirme sırasında üretilen e-postaların veya faksların konu satırında görünecek metni belirtir. Varsayılan değer boş bir dizedir. |
| [MainDocumentType](../../aspose.words.settings/mailmergesettings/maindocumenttype/) { get; set; } | Posta birleştirme ana belge türünü belirtir. Varsayılan değer:Default . |
| [Odso](../../aspose.words.settings/mailmergesettings/odso/) { get; set; } | Office Veri Kaynağı Nesnesi (ODSO) ayarlarını belirten nesneyi alır veya ayarlar. |
| [Query](../../aspose.words.settings/mailmergesettings/query/) { get; set; } | Posta birleştirme işlemi gerçekleştirildiğinde belgeye aktarılacak kayıt kümesini döndürmek için belirtilen harici veri kaynağına karşı çalıştırılacak Yapılandırılmış Sorgu Dili dizesini içerir. Varsayılan değer boş bir dizedir. |
| [ViewMergedData](../../aspose.words.settings/mailmergesettings/viewmergeddata/) { get; set; } | Microsoft Word'ün birleştirme alanlarının eklendiği belirtilen harici veri kaynağından gelen verileri görüntülemesini belirtir (örneğin birleştirilmiş verileri önizleme). Varsayılan değer:`YANLIŞ` . |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clear](../../aspose.words.settings/mailmergesettings/clear/)() | Belge kaydedildiğinde, hiçbir posta birleştirme ayarının kaydedilmeyeceği ve normal bir belge haline geleceği şekilde posta birleştirme ayarlarını temizler. |
| [Clone](../../aspose.words.settings/mailmergesettings/clone/)() | Bu nesnenin derin bir klonunu döndürür. |

## Notlar

Bu nesneyi bir belge için bir posta birleştirme veri kaynağı belirtmek için kullanabilirsiniz ve bu bilgi (mevcut veri alanlarıyla birlikte) kullanıcı bu belgeyi açtığında Microsoft Word'de görünür. Veya bu nesneyi, kullanıcının bu belge için Microsoft Word'de belirttiği posta birleştirme ayarlarını sorgulamak için kullanabilirsiniz.

Bu sınıfın nesnelerini doğrudan oluşturmanız normalde gerekmez çünkü bir belgenin Posta birleştirme ayarları her zaman şu şekilde kullanılabilir:[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) mülk.

Bu belgenin bir posta birleştirme ana belgesi olup olmadığını saptamak için değerini kontrol edin[`MainDocumentType`](./maindocumenttype/) mülk.

Bir belgeden posta birleştirme ayarlarını ve veri kaynağı bilgilerini kaldırmak için kullanabilirsiniz[`Clear`](./clear/) yöntem. Aspose.Words, ise bir belgeye posta birleştirme ayarlarını yazmayacaktır.[`MainDocumentType`](./maindocumenttype/) mülk ayarlandıNotAMergeDocument veya[`DataType`](./datatype/) mülk ayarlandıNone.

Bu nesnenin özelliklerinin nasıl kullanılacağını öğrenmenin en iyi yolu, Microsoft Word'de istenen veri kaynağıyla bir belgeyi elle oluşturmak ve ardından bu belgeyi Aspose.Words kullanarak açmak ve nesnenin özelliklerini incelemektir.[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) Ve[`Odso`](./odso/) nesneler. Bu, örneğin bir veri kaynağını programlı olarak nasıl yapılandıracağınızı öğrenmek istiyorsanız, iyi bir yaklaşımdır.

Aspose.Words, farklı biçimler arasında documents yüklerken, kaydederken ve dönüştürürken posta birleştirme bilgilerini korur, ancak kendi posta birleştirmesini kullanarak gerçekleştirirken bu bilgileri kullanmaz.[`MailMerge`](../../aspose.words.mailmerging/mailmerge/) nesne.

## Örnekler

Office Veri Kaynağı Nesnesi'ndeki verilerle bir posta birleştirmenin nasıl yürütüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// "|" karakterini kullanarak ASCII dosyası biçiminde bir veri kaynağı oluşturun
// sütunları ayıran ayırıcı olarak işlev görür. İlk satır üç sütunun adlarını içerir,
// ve her bir sonraki satır, kendi değerlerine sahip bir satırdır.
string[] lines = { "FirstName|LastName|Message",
    "John|Doe|Hello! This message was created with Aspose Words mail merge." };
string dataSrcFilename = ArtifactsDir + "MailMerge.MailMergeSettings.DataSource.txt";

File.WriteAllLines(dataSrcFilename, lines);

MailMergeSettings settings = doc.MailMergeSettings;
settings.MainDocumentType = MailMergeMainDocumentType.MailingLabels;
settings.CheckErrors = MailMergeCheckErrors.Simulate;
settings.DataType = MailMergeDataType.Native;
settings.DataSource = dataSrcFilename;
settings.Query = "SELECT * FROM " + doc.MailMergeSettings.DataSource;
settings.LinkToQuery = true;
settings.ViewMergedData = true;

Assert.AreEqual(MailMergeDestination.Default, settings.Destination);
Assert.False(settings.DoNotSupressBlankLines);

Odso odso = settings.Odso;
odso.DataSource = dataSrcFilename;
odso.DataSourceType = OdsoDataSourceType.Text;
odso.ColumnDelimiter = '|';
odso.FirstRowContainsColumnNames = true;

Assert.AreNotSame(odso, odso.Clone());
Assert.AreNotSame(settings, settings.Clone());

 // Bu belgeyi Microsoft Word'de açmak, içerikleri görüntülemeden önce posta birleştirme işlemini gerçekleştirecektir.
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)
