---
title: StructuredDocumentTagCollection Class
linktitle: StructuredDocumentTagCollection
articleTitle: StructuredDocumentTagCollection
second_title: .NET için Aspose.Words
description: Yapılandırılmış belge etiketlerinin etkili yönetimi için Aspose.Words.Markup.StructuredDocumentTagCollection sınıfını keşfedin ve belge işleme yeteneklerinizi geliştirin.
type: docs
weight: 4760
url: /tr/net/aspose.words.markup/structureddocumenttagcollection/
---
## StructuredDocumentTagCollection class

Bir koleksiyon[`IStructuredDocumentTag`](../istructureddocumenttag/) belirtilen aralıktaki yapılandırılmış belge etiketlerini temsil eden örnekler.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yapılandırılmış Belge Etiketleri veya İçerik Denetimi](https://docs.aspose.com/words/net/working-with-content-control-sdt/) belgeleme makalesi.

```csharp
public class StructuredDocumentTagCollection : IEnumerable<IStructuredDocumentTag>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.markup/structureddocumenttagcollection/count/) { get; } | Koleksiyondaki yapılandırılmış belge etiketlerinin sayısını döndürür. |
| [Item](../../aspose.words.markup/structureddocumenttagcollection/item/) { get; } | Belirtilen dizindeki yapılandırılmış belge etiketini döndürür. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetById](../../aspose.words.markup/structureddocumenttagcollection/getbyid/)(*int*) | Tanımlayıcıya göre yapılandırılmış belge etiketini döndürür. |
| [GetByTag](../../aspose.words.markup/structureddocumenttagcollection/getbytag/)(*string*) | Belirtilen etikete sahip koleksiyonda karşılaşılan ilk yapılandırılmış belge etiketini döndürür. |
| [GetByTitle](../../aspose.words.markup/structureddocumenttagcollection/getbytitle/)(*string*) | Belirtilen başlığa sahip koleksiyonda karşılaşılan ilk yapılandırılmış belge etiketini döndürür. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagcollection/getenumerator/)() | Bir numaralandırıcı nesnesi döndürür. |
| [Remove](../../aspose.words.markup/structureddocumenttagcollection/remove/)(*int*) | Belirtilen tanımlayıcıya sahip yapılandırılmış belge etiketini kaldırır. |
| [RemoveAt](../../aspose.words.markup/structureddocumenttagcollection/removeat/)(*int*) | Belirtilen dizindeki yapılandırılmış belge etiketini kaldırır. |

## Örnekler

Yapılandırılmış belge etiketinin nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Id'ye göre yapılandırılmış belge etiketini al.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsMultiSection);
Console.WriteLine(sdt.Title);

// Başlığa göre yapılandırılmış belge etiketini veya aralıklı etiketi alın.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Ayrıca bakınız

* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)
