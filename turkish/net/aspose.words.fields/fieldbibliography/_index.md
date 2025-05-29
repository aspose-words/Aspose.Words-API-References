---
title: FieldBibliography Class
linktitle: FieldBibliography
articleTitle: FieldBibliography
second_title: .NET için Aspose.Words
description: Belgelerinizdeki bibliyografya alanlarını zahmetsizce yönetmek için Aspose.Words.Fields.FieldBibliography sınıfını keşfedin. Yazınızı kolaylıkla geliştirin!
type: docs
weight: 2050
url: /tr/net/aspose.words.fields/fieldbibliography/
---
## FieldBibliography class

BIBLIYOGRAFYA alanını uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class FieldBibliography : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldBibliography](fieldbibliography/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [FilterLanguageId](../../aspose.words.fields/fieldbibliography/filterlanguageid/) { get; set; } | Bibliyografik verileri yalnızca belgedeki bu dili kullanan kaynaklara filtrelemek için kullanılan dil kimliğini alır veya ayarlar. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir tane alır[`FieldFormat`](../fieldformat/)alanın biçimlendirmesine yazılmış erişim sağlayan nesne. |
| [FormatLanguageId](../../aspose.words.fields/fieldbibliography/formatlanguageid/) { get; set; } | Belgedeki bibliyografik kaynakları biçimlendirmek için kullanılan dil kimliğini alır veya ayarlar. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcısı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcısını temsil eden düğümü alır.`hükümsüz` . |
| [SourceTag](../../aspose.words.fields/fieldbibliography/sourcetag/) { get; set; } | Kaynakçada yalnızca Etiket öğesi değeriyle eşleşen kaynakların görüntülenmesini sağlayacak bir değer alır veya ayarlar. |
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

Belgenin Kaynakça bölümünün içeriğini bibliyografik bir biçimde ekler.

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

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
