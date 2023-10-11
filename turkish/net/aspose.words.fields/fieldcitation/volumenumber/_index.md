---
title: FieldCitation.VolumeNumber
second_title: Aspose.Words for .NET API Referansı
description: FieldCitation mülk. Alıntıyla ilişkili cilt numarasını alır veya ayarlar.
type: docs
weight: 110
url: /tr/net/aspose.words.fields/fieldcitation/volumenumber/
---
## FieldCitation.VolumeNumber property

Alıntıyla ilişkili cilt numarasını alır veya ayarlar.

```csharp
public string VolumeNumber { get; set; }
```

### Örnekler

CITATION ve KAYNAKÇA alanlarıyla nasıl çalışılacağını gösterir.

```csharp
// İçinde bulabileceğimiz bibliyografik kaynakları içeren bir belge açın
// Referanslar aracılığıyla Microsoft Word -> Alıntılar ve Alıntılar Kaynakça -> Kaynakları Yönetin.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// Yalnızca sayfa numarasını ve başvurulan kitabın yazarını içeren bir alıntı oluşturun.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// Kaynaklara etiket adlarını kullanarak başvuruyoruz.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// İki kaynağa atıfta bulunan daha ayrıntılı bir alıntı oluşturun.
builder.InsertParagraph();
builder.Write("Text to be cited with two sources.");
fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);
fieldCitation.SourceTag = "Book1";
fieldCitation.AnotherSourceTag = "Book2";
fieldCitation.FormatLanguageId = "en-US";
fieldCitation.PageNumber = "19";
fieldCitation.Prefix = "Prefix ";
fieldCitation.Suffix = " Suffix";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = false;
fieldCitation.SuppressYear = false;
fieldCitation.VolumeNumber = "VII";

Assert.AreEqual(" CITATION  Book1 \\m Book2 \\l en-US \\p 19 \\f \"Prefix \" \\s \" Suffix\" \\v VII", fieldCitation.GetFieldCode());

// Belge içindeki tüm kaynakları görüntülemek için BİBLİYOGRAFYA alanını kullanabiliriz.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "5129";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 5129", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### Ayrıca bakınız

* class [FieldCitation](../)
* ad alanı [Aspose.Words.Fields](../../fieldcitation/)
* toplantı [Aspose.Words](../../../)


