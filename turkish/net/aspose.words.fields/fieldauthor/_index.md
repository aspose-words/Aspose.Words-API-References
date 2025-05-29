---
title: FieldAuthor Class
linktitle: FieldAuthor
articleTitle: FieldAuthor
second_title: .NET için Aspose.Words
description: Gelişmiş belge yönetimi ve otomasyonu için AUTHOR alanını zahmetsizce uygulamak üzere tasarlanmış Aspose.Words.Fields.FieldAuthor sınıfını keşfedin.
type: docs
weight: 1980
url: /tr/net/aspose.words.fields/fieldauthor/
---
## FieldAuthor class

AUTHOR alanını uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class FieldAuthor : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldAuthor](fieldauthor/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AuthorName](../../aspose.words.fields/fieldauthor/authorname/) { get; set; } | Belge yazarının adını alır veya ayarlar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir tane alır[`FieldFormat`](../fieldformat/)alanın biçimlendirmesine yazılmış erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcısı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcısını temsil eden düğümü alır.`hükümsüz` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son alt 'siyse, üst paragrafını döndürür. Alan zaten kaldırılmışsa, şunu döndürür`hükümsüz` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Alan bağlantısını kaldırma işlemini gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |

## Notlar

Belge yazarının adını, kaydedildiği şekilde alır ve isteğe bağlı olarak ayarlar.**Yazar** the yerleşik belge özelliklerinin özelliği.

## Örnekler

Bir belge oluşturucusunun adını görüntülemek için AUTHOR alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// AUTHOR alanları sonuçlarını "Author" adlı yerleşik belge özelliğinden alır.
// Microsoft Word'de bir belge oluşturup kaydedersek,
// o özellikte kullanıcı adımız bulunacak.
// Ancak, Aspose.Words kullanarak programatik olarak bir belge oluşturursak,
// "Yazar" özelliği varsayılan olarak boş bir dize olacaktır.
Assert.AreEqual(string.Empty, doc.BuiltInDocumentProperties.Author);

// AUTHOR alanları için kullanılacak bir yedek yazar adı ayarlayın
// "Yazar" özelliği boş bir dize içeriyorsa.
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("Joe Bloggs", field.Result);

// Bir değer içeren bir AUTHOR alanını güncelleme
// bu değeri "Yazar" yerleşik özelliğine uygulayacaktır.
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// Bu özelliği değiştirip ardından AUTHOR alanını güncellediğinizde bu değer alana uygulanacaktır.
doc.BuiltInDocumentProperties.Author = "John Doe";
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

// "Ad" özelliğini değiştirdikten sonra bir AUTHOR alanını güncellersek,
// daha sonra alan yeni adı görüntüler ve yeni adı yerleşik özelliğe uygular.
field.AuthorName = "Jane Doe";
field.Update();

Assert.AreEqual(" AUTHOR  \"Jane Doe\"", field.GetFieldCode());
Assert.AreEqual("Jane Doe", field.Result);

// AUTHOR alanları DefaultDocumentAuthor özelliğini etkilemez.
Assert.AreEqual("Jane Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Joe Bloggs", doc.FieldOptions.DefaultDocumentAuthor);

doc.Save(ArtifactsDir + "Field.AUTHOR.docx");
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
