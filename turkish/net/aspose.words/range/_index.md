---
title: Range Class
linktitle: Range
articleTitle: Range
second_title: .NET için Aspose.Words
description: Belge bölümlerini zahmetsizce yönetmenin anahtarı olan Aspose.Words.Range sınıfını keşfedin. Belge işlemenizi kusursuz kontrol ve esneklikle geliştirin.
type: docs
weight: 5250
url: /tr/net/aspose.words/range/
---
## Range class

Bir belgedeki bitişik bir alanı temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Aralıklarla Çalışma](https://docs.aspose.com/words/net/working-with-ranges/) belgeleme makalesi.

```csharp
public class Range : IEnumerable<Node>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Bookmarks](../../aspose.words/range/bookmarks/) { get; } | Bir[`Bookmarks`](./bookmarks/) . aralığındaki tüm yer imlerini temsil eden koleksiyon |
| [Fields](../../aspose.words/range/fields/) { get; } | Bir[`Fields`](./fields/) aralığındaki tüm alanları temsil eden koleksiyon |
| [FormFields](../../aspose.words/range/formfields/) { get; } | Bir[`FormFields`](./formfields/) aralıktaki tüm form alanlarını temsil eden koleksiyon. |
| [Revisions](../../aspose.words/range/revisions/) { get; } | Bu aralıkta bulunan revizyonların (izlenen değişikliklerin) bir koleksiyonunu alır. |
| [StructuredDocumentTags](../../aspose.words/range/structureddocumenttags/) { get; } | Bir[`StructuredDocumentTags`](./structureddocumenttags/) . aralığındaki tüm yapılandırılmış belge etiketlerini temsil eden koleksiyon |
| [Text](../../aspose.words/range/text/) { get; } | Aralığın metnini alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Delete](../../aspose.words/range/delete/)() | Aralığın tüm karakterlerini siler. |
| [GetEnumerator](../../aspose.words/range/getenumerator/)() |  |
| [NormalizeFieldTypes](../../aspose.words/range/normalizefieldtypes/)() | Alan türü değerlerini değiştirir[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) ile ilgili[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) bu aralıktadır, böylece alan kodlarında bulunan alan türlerine karşılık gelirler. |
| [Replace](../../aspose.words/range/replace/#replace_2)(*Regex, string*) | Bir düzenli ifade tarafından belirtilen bir karakter deseninin tüm oluşumlarını başka bir dizeyle değiştirir. |
| [Replace](../../aspose.words/range/replace/#replace)(*string, string*) | Belirtilen karakter dizisi deseninin tüm oluşumlarını bir değiştirme dizesiyle değiştirir. |
| [Replace](../../aspose.words/range/replace/#replace_3)(*Regex, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Bir düzenli ifade tarafından belirtilen bir karakter deseninin tüm oluşumlarını başka bir dizeyle değiştirir. |
| [Replace](../../aspose.words/range/replace/#replace_1)(*string, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Belirtilen karakter dizisi deseninin tüm oluşumlarını bir değiştirme dizesiyle değiştirir. |
| [ToDocument](../../aspose.words/range/todocument/)() | Aralığı içeren yeni, tam olarak oluşturulmuş bir belge oluşturur. |
| [UnlinkFields](../../aspose.words/range/unlinkfields/)() | Bu aralıktaki alanların bağlantısını kaldırır. |
| [UpdateFields](../../aspose.words/range/updatefields/)() | Bu aralıktaki belge alanlarının değerlerini günceller. |

## Notlar

Belge, düğümlerden oluşan bir ağaç tarafından temsil edilir ve düğümler, ağaçla çalışmak için operations sağlar, ancak document bitişik bir metin dizisi olarak ele alındığında bazı işlemlerin gerçekleştirilmesi daha kolaydır.

`Range` document düğümlerinin ağaç benzeri bir nesne modelinde depolanması gerçeğinden bağımsız olarak document veya belgenin bölümlerini "düz" metin olarak ele alan yöntemler sağlayan bir "cephe" arayüzüdür.

`Range` herhangi bir metin veya düğüm içermez, yalnızca bir belge parçası üzerinde bir görünüm veya "pencere" 'dir.

## Örnekler

Bir aralığın kapsadığı tüm düğümlerin metin içeriklerinin nasıl alınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### Ayrıca bakınız

* class [Node](../node/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
