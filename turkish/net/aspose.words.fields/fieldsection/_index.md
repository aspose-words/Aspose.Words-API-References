---
title: FieldSection
second_title: Aspose.Words for .NET API Referansı
description: BÖLÜM alanını uygular.
type: docs
weight: 2210
url: /tr/net/aspose.words.fields/fieldsection/
---
## FieldSection class

BÖLÜM alanını uygular.

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
| [Format](../../aspose.words.fields/field/format/) { get; } | [`FieldFormat`](../fieldformat/) alanın biçimlendirmesine yazılı erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. null. olabilir |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alandan hemen sonra bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğu ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa, döner **hükümsüz** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Bağlantıyı kaldır alanını gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |

### Notlar

Geçerli bölümün numarasını alır.

### Örnekler

Sayfaları bölümlere göre numaralandırmak için BÖLÜM ve BÖLÜM SAYFALARI alanlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Right;

// Bir BÖLÜM alanı, içinde bulunduğu bölümün numarasını görüntüler.
builder.Write("Section ");
FieldSection fieldSection = (FieldSection)builder.InsertField(FieldType.FieldSection, true);

Assert.AreEqual(" SECTION ", fieldSection.GetFieldCode());

// Bir SAYFA alanı, içinde bulunduğu sayfanın numarasını görüntüler.
builder.Write("\nPage ");
FieldPage fieldPage = (FieldPage)builder.InsertField(FieldType.FieldPage, true);

Assert.AreEqual(" PAGE ", fieldPage.GetFieldCode());

// SECTIONPAGES alanı, içinde bulunduğu bölümün kapsadığı sayfa sayısını görüntüler.
builder.Write(" of ");
FieldSectionPages fieldSectionPages = (FieldSectionPages)builder.InsertField(FieldType.FieldSectionPages, true);

Assert.AreEqual(" SECTIONPAGES ", fieldSectionPages.GetFieldCode());

// Başlıktan ana belgeye geri dönün ve iki sayfa ekleyin.
// Tüm bu sayfalar ilk bölümde olacak. Her başlıkta bir kez görünen alanlarımız,
// bu bölümün mevcut/toplam sayfalarını numaralandıracaktır.
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// Belge oluşturucu ile bu şekilde yeni bir bölüm ekleyebiliriz.
// Bu, sonraki tüm başlıklarda BÖLÜM ve BÖLÜM SAYFALARI alanlarında görüntülenen değerleri etkileyecektir.
builder.InsertBreak(BreakType.SectionBreakNewPage);

// SAYFA alanı, tüm belge boyunca sayfaları saymaya devam edecektir.
// Sayfaları bölüm bölüm takip etmek için her bölümde sayısını manuel olarak sıfırlayabiliriz.
builder.CurrentSection.PageSetup.RestartPageNumbering = true;
builder.InsertBreak(BreakType.PageBreak);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SECTION.SECTIONPAGES.docx");
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
