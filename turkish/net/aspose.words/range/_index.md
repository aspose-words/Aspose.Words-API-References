---
title: Class Range
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Range sınıf. Bir belgedeki bitişik bir alanı temsil eder.
type: docs
weight: 4520
url: /tr/net/aspose.words/range/
---
## Range class

Bir belgedeki bitişik bir alanı temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Aralıklarla Çalışmak](https://docs.aspose.com/words/net/working-with-ranges/) dokümantasyon makalesi.

```csharp
public class Range
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Bookmarks](../../aspose.words/range/bookmarks/) { get; } | Bir değeri döndürür[`Bookmarks`](./bookmarks/) aralıktaki tüm yer işaretlerini temsil eden koleksiyon. |
| [Fields](../../aspose.words/range/fields/) { get; } | Bir değeri döndürür[`Fields`](./fields/) aralıktaki tüm alanları temsil eden koleksiyon. |
| [FormFields](../../aspose.words/range/formfields/) { get; } | Bir değeri döndürür[`FormFields`](./formfields/) aralıktaki tüm form alanlarını temsil eden koleksiyon. |
| [Revisions](../../aspose.words/range/revisions/) { get; } | Bu aralıkta mevcut olan revizyonların (izlenen değişiklikler) bir koleksiyonunu alır. |
| [StructuredDocumentTags](../../aspose.words/range/structureddocumenttags/) { get; } | Bir değeri döndürür[`StructuredDocumentTags`](./structureddocumenttags/) aralıktaki tüm yapılandırılmış belge etiketlerini temsil eden koleksiyon. |
| [Text](../../aspose.words/range/text/) { get; } | Aralığın metnini alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Delete](../../aspose.words/range/delete/)() | Aralığın tüm karakterlerini siler. |
| [NormalizeFieldTypes](../../aspose.words/range/normalizefieldtypes/)() | Alan türü değerlerini değiştirir[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) ile ilgili[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) alan kodlarında yer alan alan türlerine karşılık gelecek şekilde bu aralıkta. |
| [Replace](../../aspose.words/range/replace/#replace_2)(Regex, string) | Normal bir ifadeyle belirtilen karakter modelinin tüm oluşumlarını başka bir dizeyle değiştirir. |
| [Replace](../../aspose.words/range/replace/#replace)(string, string) | Belirtilen karakter dizisi modelinin tüm oluşumlarını bir değiştirme dizesiyle değiştirir. |
| [Replace](../../aspose.words/range/replace/#replace_3)(Regex, string, FindReplaceOptions) | Normal bir ifadeyle belirtilen karakter modelinin tüm oluşumlarını başka bir dizeyle değiştirir. |
| [Replace](../../aspose.words/range/replace/#replace_1)(string, string, FindReplaceOptions) | Belirtilen karakter dizisi modelinin tüm oluşumlarını bir değiştirme dizesiyle değiştirir. |
| [ToDocument](../../aspose.words/range/todocument/)() | Aralığı içeren tam biçimli yeni bir belge oluşturur. |
| [UnlinkFields](../../aspose.words/range/unlinkfields/)() | Bu aralıktaki alanların bağlantısını kaldırır. |
| [UpdateFields](../../aspose.words/range/updatefields/)() | Bu aralıktaki belge alanlarının değerlerini günceller. |

### Notlar

Belge bir düğüm ağacıyla temsil edilir ve düğümler ağaçla çalışmak için işlem 'yi sağlar, ancak belge bitişik bir metin dizisi olarak ele alınırsa bazı işlemlerin gerçekleştirilmesi daha kolaydır.

`Range`document düğümlerinin ağaç benzeri bir nesne modelinde saklanmasına bakılmaksızın document veya belgenin bölümlerini "düz" metin olarak ele alan yöntemler sağlayan bir "cephe" arayüzüdür.

`Range` herhangi bir metin veya düğüm içermez, yalnızca bir belgenin bir parçası üzerindeki bir görünüm veya "pencere" 'dir.

### Örnekler

Bir aralığın kapsadığı tüm düğümlerin metin içeriklerinin nasıl alınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


