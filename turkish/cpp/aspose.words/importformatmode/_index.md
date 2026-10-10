---
title: "Aspose::Words::ImportFormatMode enum"
linktitle: "ImportFormatMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ImportFormatMode enum. Başka bir belgeden içerik içe aktarılırken biçimlendirmelerin nasıl birleştirileceğini belirtir C++'da."
type: docs
weight: 93000
url: /tr/cpp/aspose.words/importformatmode/
---
## ImportFormatMode enum


Başka bir belgeden içerik içe aktarılırken biçimlendirmenin nasıl birleştirileceğini belirtir.

```cpp
enum class ImportFormatMode
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| UseDestinationStyles | 0 | Hedef belge stillerini kullan ve yeni stilleri kopyala. Bu varsayılan seçenektir. |
| KeepSourceFormatting | 1 | Gerekli tüm stilleri hedef belgeye kopyala, gerekirse benzersiz stil adları oluştur. |
| KeepDifferentStyles | 2 | Yalnızca kaynak belgedeki stillerden farklı olan stilleri kopyalayın. |

## Açıklamalar


Bir belgeden diğerine düğümleri kopyaladığınızda, bu seçenek her iki belgenin aynı ada sahip ancak farklı biçimlendirmeye sahip bir stili olduğunda biçimlendirmenin nasıl çözümleneceğini belirtir.

Biçimlendirme aşağıdaki gibi çözülür:

1. Yerleşik stiller, bölge bağımsız stil tanımlayıcıları kullanılarak eşleştirilir. Kullanıcı tanımlı stiller, büyük/küçük harfe duyarlı stil adı kullanılarak eşleştirilir.
1. Hedef belgede eşleşen bir stil bulunamazsa, stil (ve ona referans veren tüm stiller) hedef belgeye kopyalanır ve içe aktarılan düğümler yeni stile referans gösterecek şekilde güncellenir.
1. Hedef belgede eşleşen bir stil zaten mevcutsa, ne olacağı aşağıda açıklandığı gibi [ImportNode()](../) yöntemine geçirilen **importFormatMode** parametresine bağlıdır.



[UseDestinationStyles](./) seçeneği kullanılırken, hedef belgede eşleşen bir stil zaten mevcutsa, stil kopyalanmaz ve içe aktarılan düğümler mevcut stile referans gösterecek şekilde güncellenir.

[UseDestinationStyles](./) kullanmanın dezavantajı, içe aktarılan metnin hedef belgede kaynak belgeye kıyasla farklı görünebilmesidir. Örneğin, kaynak belgedeki "Heading 1" stili Arial 16pt yazı tipini, hedef belgedeki "Heading 1" stili ise Times New Roman 14pt yazı tipini kullanır. "Heading 1" stilindeki metin başka doğrudan biçimlendirme olmadan içe aktarıldığında, hedef belgede Times New Roman 14pt olarak görünecektir.

[KeepSourceFormatting](./) option allows to make sure the imported content looks the same in the destination document like it looks in the source document. If a matching style already exists in the destination document, the source style formatting is expanded into direct [Node](../node/) attributes and the style is changed to Normal. If the style does not exist in the destination document, then the source style is imported into the destination document and applied to the imported node. Note, that it is not always possible to preserve the source style even if it does not exist in the destination document. In this case formatting of such style will be expanded into direct [Node](../node/) attributes in favor of preserving original [Node](../node/) formatting.

[KeepSourceFormatting](./) kullanmanın dezavantajı, birden fazla içe aktarma yaptığınızda hedef belgede çok sayıda stil birikmesi ve bunun bu belgede Microsoft Word'de tutarlı stil biçimlendirmesi kullanmayı zorlaştırmasıdır.

[KeepDifferentStyles](./) seçeneğini kullanmak, sağladıkları biçimlendirme kaynak belgedeki stillerle aynıysa hedef stillerin yeniden kullanılmasına izin verir. Hedef belgedeki stil kaynakla farklıysa stil içe aktarılır.

## Örnekler



Bir belgenin başka bir belgeye nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

auto docToInsert = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Formatted elements.docx");

builder->InsertDocument(docToInsert, Aspose::Words::ImportFormatMode::KeepSourceFormatting);
builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertDocument.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
