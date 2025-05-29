---
title: FieldCitation.VolumeNumber
linktitle: VolumeNumber
articleTitle: VolumeNumber
second_title: .NET için Aspose.Words
description: FieldCitation VolumeNumber özelliğiyle alıntılarınızı zahmetsizce yönetin; ilişkili cilt numaralarını kolayca ayarlayabilir veya alabilirsiniz.
type: docs
weight: 110
url: /tr/net/aspose.words.fields/fieldcitation/volumenumber/
---
## FieldCitation.VolumeNumber property

Alıntıyla ilişkili bir cilt numarası alır veya ayarlar.

```csharp
public string VolumeNumber { get; set; }
```

## Örnekler

CITATION ve BIBLIYOGRAFYA alanlarıyla nasıl çalışılacağını gösterir.

```csharp
// İçinde bibliyografik kaynaklar bulunan bir belgeyi aç
// Microsoft Word aracılığıyla Referanslar -> Alıntılar ve Kaynakça -> Kaynakları Yönet.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// Sadece sayfa numarası ve atıfta bulunulan kitabın yazarı ile bir atıf oluşturun.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// Kaynaklara etiket adlarını kullanarak atıfta bulunuyoruz.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// İki kaynağı da gösteren daha detaylı bir alıntı oluşturun.
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

// Belgedeki tüm kaynakları görüntülemek için BIBLIOGRAPHY alanını kullanabiliriz.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "5129";
fieldBibliography.FilterLanguageId = "5129";
fieldBibliography.SourceTag = "Book2";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 5129 \\f 5129 \\m Book2", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### Ayrıca bakınız

* class [FieldCitation](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
