---
title: FieldIndex.PageNumberSeparator
linktitle: PageNumberSeparator
articleTitle: PageNumberSeparator
second_title: .NET için Aspose.Words
description: FieldIndex PageNumberSeparator özelliğini keşfedin, dizin girişlerini sayfa numaralarından ayıran karakteri kolayca özelleştirerek daha net hale getirin.
type: docs
weight: 120
url: /tr/net/aspose.words.fields/fieldindex/pagenumberseparator/
---
## FieldIndex.PageNumberSeparator property

Bir dizin girişini ve sayfa numarasını ayırmak için kullanılan karakter dizisini alır veya ayarlar.

```csharp
public string PageNumberSeparator { get; set; }
```

## Örnekler

INDEX alanındaki sayfa numarası ayırıcısının nasıl düzenleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir girdi görüntüleyecek bir INDEX alanı oluşturun.
// Her giriş, sol tarafta XE alanının Metin özelliği değerini görüntüler,
// ve sağ tarafta XE alanını içeren sayfanın numarası.
// INDEX girişi, "Metin" özelliğindeki eşleşen değerlere sahip XE alanlarını gruplayacaktır
// her XE alanı için bir giriş yapmak yerine, tek bir girişe.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// INDEX alanımızda bir grup XE alanı için bir giriş varsa,
// bu giriş, bu gruba ait bir XE alanı içeren her sayfanın numarasını görüntüler.
// Bu sayfa numaralarının görünümünü özelleştirmek için özel ayraçlar ayarlayabiliriz.
index.PageNumberSeparator = ", on page(s) ";
index.PageNumberListSeparator = " & ";

Assert.AreEqual(" INDEX  \\e \", on page(s) \" \\l \" & \"", index.GetFieldCode());
Assert.True(index.HasPageNumberSeparator);

// Bu XE alanlarını ekledikten sonra, INDEX alanı "İlk giriş, 2., 3. ve 4. sayfalarda" ifadesini gösterecektir.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

Assert.AreEqual(" XE  \"First entry\"", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.PageNumberList.docx");
```

### Ayrıca bakınız

* class [FieldIndex](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
