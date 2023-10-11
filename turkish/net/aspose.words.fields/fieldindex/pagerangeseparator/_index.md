---
title: FieldIndex.PageRangeSeparator
second_title: Aspose.Words for .NET API Referansı
description: FieldIndex mülk. Sayfa aralığının başlangıcını ve sonunu ayırmak için kullanılan karakter sırasını alır veya ayarlar.
type: docs
weight: 130
url: /tr/net/aspose.words.fields/fieldindex/pagerangeseparator/
---
## FieldIndex.PageRangeSeparator property

Sayfa aralığının başlangıcını ve sonunu ayırmak için kullanılan karakter sırasını alır veya ayarlar.

```csharp
public string PageRangeSeparator { get; set; }
```

### Örnekler

Bir yer iminin yayılmış sayfalarının bir INDEX alanı girişi için sayfa aralığı olarak nasıl belirtileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir giriş görüntüleyecek bir INDEX alanı oluşturun.
// Her girişte XE alanının Text özelliği değeri sol tarafta görüntülenecektir,
// ve sağdaki XE alanını içeren sayfanın numarası.
// INDEX girişi "Text" özelliğinde eşleşen değerlere sahip tüm XE alanlarını toplayacaktır
// her XE alanı için bir giriş yapmak yerine tek bir girişe.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Sayfa aralıklarını görüntüleyen INDEX girişleri için bir ayırıcı dize belirtebiliriz
// ilk sayfanın numarası ile son sayfanın numarası arasında görünecek.
index.PageNumberSeparator = ", on page(s) ";
index.PageRangeSeparator = " to ";

Assert.AreEqual(" INDEX  \\e \", on page(s) \" \\g \" to \"", index.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "My entry";

// Bir XE alanı PageRangeBookmarkName özelliğini kullanarak bir yer imini adlandırırsa,
// INDEX girişi, yer iminin kapsadığı sayfa aralığını gösterecektir
// XE alanını içeren sayfanın numarası yerine.
indexEntry.PageRangeBookmarkName = "MyBookmark";

Assert.AreEqual(" XE  \"My entry\" \\r MyBookmark", indexEntry.GetFieldCode());
Assert.AreEqual("MyBookmark", indexEntry.PageRangeBookmarkName);

// 3. sayfada başlayan ve 5. sayfada biten bir yer imi ekleyin.
// Bu yer imine başvuran XE alanı için INDEX girişi bu sayfa aralığını görüntüleyecektir.
// Tablomuzdaki INDEX girişi "Girişimim, sayfa 3'ten 5'e kadar" olarak görünecektir.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MyBookmark");
builder.Write("Start of MyBookmark");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.Write("End of MyBookmark");
builder.EndBookmark("MyBookmark");

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.PageRangeBookmark.docx");
```

### Ayrıca bakınız

* class [FieldIndex](../)
* ad alanı [Aspose.Words.Fields](../../fieldindex/)
* toplantı [Aspose.Words](../../../)


