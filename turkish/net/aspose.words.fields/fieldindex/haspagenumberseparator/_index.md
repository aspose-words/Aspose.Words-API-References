---
title: FieldIndex.HasPageNumberSeparator
linktitle: HasPageNumberSeparator
articleTitle: HasPageNumberSeparator
second_title: .NET için Aspose.Words
description: Gelişmiş belge biçimlendirmesi için alan kodu aracılığıyla bir sayfa numarası ayırıcısının özelleştirilip özelleştirilmediğini ortaya çıkaran FieldIndex HasPageNumberSeparator özelliğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.fields/fieldindex/haspagenumberseparator/
---
## FieldIndex.HasPageNumberSeparator property

Sayfa numarası ayırıcısının alanın kodu aracılığıyla geçersiz kılınıp kılınmadığını belirten bir değer alır.

```csharp
public bool HasPageNumberSeparator { get; }
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
