---
title: ImportFormatMode Enum
linktitle: ImportFormatMode
articleTitle: ImportFormatMode
second_title: Aspose.Words for .NET
description: Aspose.Words.ImportFormatMode Sıralama. Başka bir belgeden içerik içe aktarılırken biçimlendirmenin nasıl birleştirileceğini belirtir C#'da.
type: docs
weight: 3230
url: /tr/net/aspose.words/importformatmode/
---
## ImportFormatMode enumeration

Başka bir belgeden içerik içe aktarılırken biçimlendirmenin nasıl birleştirileceğini belirtir.

```csharp
public enum ImportFormatMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| UseDestinationStyles | `0` | Hedef belge stillerini kullanın ve yeni stilleri kopyalayın. Bu varsayılan seçenektir. |
| KeepSourceFormatting | `1` | Gerekli tüm stilleri hedef belgeye kopyalayın, gerekirse benzersiz stil adları oluşturun. |
| KeepDifferentStyles | `2` | Yalnızca kaynak belgedekilerden farklı stilleri kopyalayın. |

## Notlar

Düğümleri bir belgeden diğerine kopyaladığınızda bu seçenek, her iki belge de aynı ada ancak farklı biçimlendirmeye sahip bir stile sahip olduğunda formatting 'nin nasıl çözümleneceğini belirtir.

Biçimlendirme şu şekilde çözülür:

1. Yerleşik stiller, yerel ayarlardan bağımsız stil tanımlayıcıları kullanılarak eşleştirilir. Kullanıcı tanımlı stiller, büyük/küçük harfe duyarlı stil adı kullanılarak eşleştirilir.
2. Hedef belgede eşleşen bir stil bulunamazsa, style (ve onun tarafından başvurulan tüm stiller) hedef document 'ye kopyalanır ve içe aktarılan düğümler yeni stile referans verecek şekilde güncellenir.
3. Hedef belgede eşleşen bir stil zaten mevcutsa ne olacağı ,`içe aktarmaFormatMode` parametre 'ye aktarıldı[`Document.ImportNode`](../documentbase/importnode/) aşağıda açıklandığı gibi.

KullanırkenUseDestinationStyles seçeneği, hedef belgede eşleşen bir stil zaten mevcutsa , stil kopyalanmaz ve içe aktarılan düğümler mevcut stile referans vermek üzere güncellenir .

Kullanmanın sakıncasıUseDestinationStylesiçe aktarılan metnin kaynak belgeyle karşılaştırıldığında hedef belgede farklı görünmesi olabilir. Örneğin, kaynak belgedeki "Başlık 1" stili Arial 16pt yazı tipini kullanır ve hedef belgedeki "Başlık 1" stili Times New'i kullanır Roman 14pt yazı tipi. "Başlık 1" stilindeki metni başka doğrudan biçimlendirme olmadan içe aktarırken, hedef belgede Times New Roman 14pt yazı tipi olarak görünecektir.

KeepSourceFormattingseçeneği, içe aktarılan içeriğin hedef belgede kaynak belgede göründüğü gibi aynı görünmesini sağlar. Hedef belgede eşleşen bir stil zaten mevcutsa, kaynak stili formatlaması doğrudan Düğüm niteliklerine genişletilir ve stil Normal olarak değiştirildi. Stil hedef belgede mevcut değilse, kaynak stil hedef belgeye import alınır ve içe aktarılan düğüme uygulanır. Kaynak stil, hedef belgede bulunsa bile her zaman korumanın mümkün olmadığını unutmayın. hedef belgede mevcut değil. Bu durumda, bu tür stilin formatlaması, orijinal Node formatının korunması lehine doğrudan Node niteliklerine genişletilecektir.

Kullanmanın sakıncasıKeepSourceFormattingbirkaç içe aktarma işlemi gerçekleştirirseniz, hedef belgede birçok stile sahip olabilirsiniz ve bu da bu belge için Microsoft Word'deki tutarlı stil biçimlendirmesinin kullanılmasını zorlaştırabilir.

KullanmaKeepDifferentStyles seçeneği, sağladıkları biçimlendirme kaynak belgedeki stillerle aynıysa hedef stilleri yeniden kullanılmasına izin verir. Hedef belgedeki stil kaynaktan farklıysa o zaman içe aktarılır.

## Örnekler

Bir belgenin başka bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.PageBreak);

Document docToInsert = new Document(MyDir + "Formatted elements.docx");

builder.InsertDocument(docToInsert, ImportFormatMode.KeepSourceFormatting);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.InsertDocument.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
