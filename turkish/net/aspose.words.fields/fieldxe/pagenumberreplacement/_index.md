---
title: FieldXE.PageNumberReplacement
linktitle: PageNumberReplacement
articleTitle: PageNumberReplacement
second_title: Aspose.Words for .NET
description: FieldXE PageNumberReplacement mülk. Sayfa numarası yerine kullanılan metni alır veya ayarlar C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words.fields/fieldxe/pagenumberreplacement/
---
## FieldXE.PageNumberReplacement property

Sayfa numarası yerine kullanılan metni alır veya ayarlar.

```csharp
public string PageNumberReplacement { get; set; }
```

## Örnekler

Bir INDEX alanında çapraz referansların nasıl tanımlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir giriş görüntüleyecek bir INDEX alanı oluşturun.
// Her girişte XE alanının Text özelliği değeri sol tarafta görüntülenecektir,
// ve sağdaki XE alanını içeren sayfanın numarası.
// INDEX girişi "Text" özelliğinde eşleşen değerlere sahip tüm XE alanlarını toplayacaktır
// her XE alanı için bir giriş yapmak yerine tek bir girişe.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Bir XE alanını, INDEX girişinin sayfa numarası yerine bir dize göstermesini sağlayacak şekilde yapılandırabiliriz.
// İlk olarak, sayfa numarasını bir dizeyle değiştiren girişler için,
// XE alanının Metin özelliği değeri ile dize arasında özel bir ayırıcı belirtin.
index.CrossReferenceSeparator = ", see: ";

Assert.AreEqual(" INDEX  \\k \", see: \"", index.GetFieldCode());

// Bu alanın sayfa numarasını görüntüleyen normal bir INDEX girişi oluşturan bir XE alanı ekleyin,
// ve CrossReferenceSeparator değerini çağırmaz.
// Bu XE alanının girişi "Apple, 2" olarak görüntülenecektir.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";

Assert.AreEqual(" XE  Apple", indexEntry.GetFieldCode());

// 3. sayfaya başka bir XE alanı ekleyin ve PageNumberReplacement özelliği için bir değer ayarlayın.
// Bu alanın bulunduğu sayfa numarası yerine bu değer görünecek,
// ve INDEX alanının CrossReferenceSeparator değeri onun önünde görünecektir.
// Bu XE alanının girişinde "Muz, bakınız: Tropikal meyve" görüntülenecektir.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";
indexEntry.PageNumberReplacement = "Tropical fruit";

Assert.AreEqual(" XE  Banana \\t \"Tropical fruit\"", indexEntry.GetFieldCode());

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.CrossReferenceSeparator.docx");
```

### Ayrıca bakınız

* class [FieldXE](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
