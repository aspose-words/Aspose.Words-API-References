---
title: FieldIndex.PageRangeSeparator
linktitle: PageRangeSeparator
articleTitle: PageRangeSeparator
second_title: .NET için Aspose.Words
description: FieldIndex'teki PageRangeSeparator özelliğini keşfedin. Sorunsuz sayfa aralığı biçimlendirmesi için karakter dizisini kolayca özelleştirin ve belgenizin netliğini artırın.
type: docs
weight: 130
url: /tr/net/aspose.words.fields/fieldindex/pagerangeseparator/
---
## FieldIndex.PageRangeSeparator property

Bir sayfa aralığının başlangıcını ve sonunu ayırmak için kullanılan karakter dizisini alır veya ayarlar.

```csharp
public string PageRangeSeparator { get; set; }
```

## Örnekler

Bir yer iminin yayılmış sayfalarının bir INDEX alan girişi için sayfa aralığı olarak nasıl belirtileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir girdi görüntüleyecek bir INDEX alanı oluşturun.
// Her giriş, sol tarafta XE alanının Metin özelliği değerini görüntüler,
// ve sağ tarafta XE alanını içeren sayfanın numarası.
// INDEX girişi, "Metin" özelliğindeki eşleşen değerlere sahip tüm XE alanlarını toplayacaktır
// her XE alanı için bir giriş yapmak yerine, tek bir girişe.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Sayfa aralıklarını görüntüleyen INDEX girişleri için bir ayırıcı dize belirtebiliriz
// ilk sayfa numarası ile son sayfa numarası arasında görünecek.
index.PageNumberSeparator = ", on page(s) ";
index.PageRangeSeparator = " to ";

Assert.AreEqual(" INDEX  \\e \", on page(s) \" \\g \" to \"", index.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "My entry";

// Bir XE alanı, PageRangeBookmarkName özelliğini kullanarak bir yer imini adlandırırsa,
// INDEX girişi, yer iminin kapsadığı sayfa aralığını gösterecektir
// XE alanını içeren sayfanın numarası yerine.
indexEntry.PageRangeBookmarkName = "MyBookmark";

Assert.AreEqual(" XE  \"My entry\" \\r MyBookmark", indexEntry.GetFieldCode());
Assert.AreEqual("MyBookmark", indexEntry.PageRangeBookmarkName);

// 3. sayfadan başlayıp 5. sayfada biten bir yer imi ekle.
// Bu yer imine başvuran XE alanı için INDEX girişi bu sayfa aralığını görüntüler.
// Tablomuzda INDEX girişi "Girişim, 3 ila 5. sayfadaki" ifadesini gösterecektir.
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
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
