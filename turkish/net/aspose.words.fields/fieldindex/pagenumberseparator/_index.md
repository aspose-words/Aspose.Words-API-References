---
title: FieldIndex.PageNumberSeparator
second_title: Aspose.Words for .NET API Referansı
description: FieldIndex mülk. Bir dizin girişini ve onun sayfa numarasını ayırmak için kullanılan karakter sırasını alır veya ayarlar.
type: docs
weight: 120
url: /tr/net/aspose.words.fields/fieldindex/pagenumberseparator/
---
## FieldIndex.PageNumberSeparator property

Bir dizin girişini ve onun sayfa numarasını ayırmak için kullanılan karakter sırasını alır veya ayarlar.

```csharp
public string PageNumberSeparator { get; set; }
```

### Örnekler

Bir INDEX alanında sayfa numarası ayırıcısının nasıl düzenleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir giriş görüntüleyecek bir INDEX alanı oluşturun.
// Her girişte XE alanının Text özelliği değeri sol tarafta görüntülenecektir,
// ve sağdaki XE alanını içeren sayfanın numarası.
// INDEX girişi, XE alanlarını "Metin" özelliğinde eşleşen değerlerle gruplandırır
// her XE alanı için bir giriş yapmak yerine tek bir girişe.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// INDEX alanımızda bir grup XE alanı için giriş varsa,
// bu giriş, bu gruba ait bir XE alanı içeren her sayfanın numarasını görüntüleyecektir.
// Bu sayfa numaralarının görünümünü özelleştirmek için özel ayırıcılar ayarlayabiliriz.
index.PageNumberSeparator = ", on page(s) ";
index.PageNumberListSeparator = " & ";

Assert.AreEqual(" INDEX  \\e \", on page(s) \" \\l \" & \"", index.GetFieldCode());
Assert.True(index.HasPageNumberSeparator);

// Bu XE alanlarını ekledikten sonra, INDEX alanında "İlk giriş, sayfa 2, 3 ve 4'te" görüntülenecektir.
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
* ad alanı [Aspose.Words.Fields](../../fieldindex/)
* toplantı [Aspose.Words](../../../)


