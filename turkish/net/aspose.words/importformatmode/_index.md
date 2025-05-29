---
title: ImportFormatMode Enum
linktitle: ImportFormatMode
articleTitle: ImportFormatMode
second_title: .NET için Aspose.Words
description: Aspose.Words.ImportFormatMode'un, içe aktarılan içeriklerden stilleri kusursuz bir şekilde birleştirerek en iyi sonuçları elde etmek için belge biçimlendirmesini nasıl geliştirdiğini keşfedin.
type: docs
weight: 3680
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
| KeepSourceFormatting | `1` | Tüm gerekli stilleri hedef belgeye kopyalayın, gerekirse benzersiz stil adları oluşturun. |
| KeepDifferentStyles | `2` | Yalnızca kaynak belgedekilerden farklı olan stilleri kopyala. |

## Notlar

Düğümleri bir belgeden diğerine kopyaladığınızda, bu seçenek, her iki belgenin de aynı ada sahip ancak farklı biçimlendirmeye sahip bir stili olduğunda formatting öğesinin nasıl çözümleneceğini belirtir.

Biçimlendirme şu şekilde çözümlenmiştir:

1. Yerleşik stiller, yerel bağımsız stil tanımlayıcıları kullanılarak eşleştirilir. Kullanıcı tarafından tanımlanan stiller, büyük/küçük harfe duyarlı stil adı kullanılarak eşleştirilir.
2. Hedef belgede eşleşen bir stil bulunamazsa, style (ve onun başvurduğu tüm stiller) hedef document 'ye kopyalanır ve içe aktarılan düğümler yeni stile başvuracak şekilde güncellenir.
3. Hedef belgede eşleşen bir stil zaten varsa, ne olacağı şuna bağlıdır:`içe aktarmaBiçimModu` parametre to 'ye geçirildi[`ImportNode`](../documentbase/importnode/) aşağıda açıklandığı gibidir.

KullanırkenUseDestinationStyles seçeneği, eşleşen bir stil hedef belgede zaten mevcutsa , stil kopyalanmaz ve içe aktarılan düğümler mevcut stile başvuracak şekilde güncellenir .

Kullanmanın dezavantajıUseDestinationStylesiçe aktarılan metnin hedef belgede kaynak belgeye göre farklı görünebileceğidir. Örneğin, kaynak belgedeki "Başlık 1" stili Arial 16pt yazı tipini kullanır ve hedef belgedeki "Başlık 1" stili Times New Roman 14pt yazı tipini kullanır. Başka bir doğrudan biçimlendirme olmadan "Başlık 1" stilindeki metni içe aktardığınızda, hedef belgede Times New Roman 14pt yazı tipi olarak görünecektir.

KeepSourceFormattingseçeneği, içe aktarılan içeriğin hedef belgede kaynak belgede göründüğü gibi görünmesini sağlar. Hedef belgede eşleşen bir stil zaten varsa, kaynak stil biçimlendirmesi doğrudan Düğüm özniteliklerine genişletilir ve stil Normal olarak değiştirilir. Stil hedef belgede yoksa, kaynak stil hedef belgeye içe aktarılır ve içe aktarılan düğüme uygulanır. Kaynak stili hedef belgede mevcut olmasa bile korumak her zaman mümkün olmayabilir. Bu durumda, bu tür stilin biçimlendirmesi orijinal Düğüm biçimlendirmesini korumak adına doğrudan Düğüm özniteliklerine genişletilecektir.

Kullanmanın dezavantajıKeepSourceFormattingEğer birden fazla içe aktarma yaparsanız, hedef belgede birçok stil ile sonuçlanabilirsiniz ve bu da bu belge için Microsoft Word'de tutarlı stil biçimlendirmesini kullanmayı zorlaştırabilir.

KullanarakKeepDifferentStyles seçeneği, sağladıkları biçimlendirme kaynak belgedeki stillerle aynıysa hedef styles öğesinin yeniden kullanılmasına izin verir. Hedef belgedeki stil kaynaktan farklıysa içe aktarılır.

## Örnekler

Bir belgenin başka bir belgenin içine nasıl ekleneceğini gösterir.

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
