---
title: FieldSection Class
linktitle: FieldSection
articleTitle: FieldSection
second_title: .NET için Aspose.Words
description: Belge işlemede SECTION alanlarını verimli bir şekilde uygulamak için çözümünüz olan Aspose.Words.Fields.FieldSection sınıfını keşfedin. İş akışınızı bugün geliştirin!
type: docs
weight: 2770
url: /tr/net/aspose.words.fields/fieldsection/
---
## FieldSection class

SECTION alanını uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class FieldSection : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldSection](fieldsection/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir tane alır[`FieldFormat`](../fieldformat/)alanın biçimlendirmesine yazılmış erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcısı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcısını temsil eden düğümü alır.`hükümsüz` . |
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

Mevcut bölümün numarasını alır.

## Örnekler

Sayfaları bölümlere göre numaralandırmak için SECTION ve SECTIONPAGES alanlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Right;

// BÖLÜM alanı, içinde bulunduğu bölümün numarasını görüntüler.
builder.Write("Section ");
FieldSection fieldSection = (FieldSection)builder.InsertField(FieldType.FieldSection, true);

Assert.AreEqual(" SECTION ", fieldSection.GetFieldCode());

// SAYFA alanı, içinde bulunduğu sayfanın numarasını görüntüler.
builder.Write("\nPage ");
FieldPage fieldPage = (FieldPage)builder.InsertField(FieldType.FieldPage, true);

Assert.AreEqual(" PAGE ", fieldPage.GetFieldCode());

// SECTIONPAGES alanı, içinde bulunduğu bölümün kapsadığı sayfa sayısını görüntüler.
builder.Write(" of ");
FieldSectionPages fieldSectionPages = (FieldSectionPages)builder.InsertField(FieldType.FieldSectionPages, true);

Assert.AreEqual(" SECTIONPAGES ", fieldSectionPages.GetFieldCode());

// Başlıktan çıkıp ana belgeye geri dön ve iki sayfa ekle.
// Tüm bu sayfalar ilk bölümde olacak. Her başlıkta bir kez görünen alanlarımız,
// Bu bölümün mevcut/toplam sayfa sayısını numaralandırır.
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// Belge oluşturucuyu kullanarak yeni bir bölüm ekleyebiliriz.
// Bu, önümüzdeki tüm başlıklardaki SECTION ve SECTIONPAGES alanlarında görüntülenen değerleri etkileyecektir.
builder.InsertBreak(BreakType.SectionBreakNewPage);

// SAYFA alanı, belgenin tamamındaki sayfaları saymaya devam edecektir.
// Sayfaları bölüm bölüm takip edebilmek için her bölümde sayısını manuel olarak sıfırlayabiliriz.
builder.CurrentSection.PageSetup.RestartPageNumbering = true;
builder.InsertBreak(BreakType.PageBreak);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SECTION.SECTIONPAGES.docx");
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
