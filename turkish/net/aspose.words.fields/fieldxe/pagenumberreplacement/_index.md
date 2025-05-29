---
title: FieldXE.PageNumberReplacement
linktitle: PageNumberReplacement
articleTitle: PageNumberReplacement
second_title: .NET için Aspose.Words
description: Gelişmiş belge biçimlendirmesi ve iyileştirilmiş okunabilirlik için sayfa numarası metnini kolayca özelleştirmek amacıyla FieldXE PageNumberReplacement özelliğini keşfedin.
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

INDEX alanında çapraz referansların nasıl tanımlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir girdi görüntüleyecek bir INDEX alanı oluşturun.
// Her giriş, sol tarafta XE alanının Metin özelliği değerini görüntüler,
// ve sağ tarafta XE alanını içeren sayfanın numarası.
// INDEX girişi, "Metin" özelliğindeki eşleşen değerlere sahip tüm XE alanlarını toplayacaktır
// her XE alanı için bir giriş yapmak yerine, tek bir girişe.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Bir XE alanını, INDEX girişinin sayfa numarası yerine bir dize görüntülemesini sağlayacak şekilde yapılandırabiliriz.
// İlk olarak, sayfa numarasını bir dizeyle değiştiren girişler için,
// XE alanının Metin özelliği değeri ile dize arasında özel bir ayırıcı belirtin.
index.CrossReferenceSeparator = ", see: ";

Assert.AreEqual(" INDEX  \\k \", see: \"", index.GetFieldCode());

// Bu alanın sayfa numarasını görüntüleyen düzenli bir DİZİN girişi oluşturan bir XE alanı ekleyin,
// ve CrossReferenceSeparator değerini çağırmaz.
// Bu XE alanına ait giriş "Apple, 2" olarak gösterilecektir.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";

Assert.AreEqual(" XE  Apple", indexEntry.GetFieldCode());

// 3. sayfaya başka bir XE alanı ekleyin ve PageNumberReplacement özelliği için bir değer belirleyin.
// Bu değer, bu alanın bulunduğu sayfanın numarası yerine gösterilecektir.
// ve INDEX alanının CrossReferenceSeparator değeri bunun önünde görünecektir.
// Bu XE alanının girişi "Muz, bkz: Tropikal meyve" ifadesini gösterecektir.
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
