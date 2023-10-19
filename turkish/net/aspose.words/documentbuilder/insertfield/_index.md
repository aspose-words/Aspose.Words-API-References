---
title: DocumentBuilder.InsertField
linktitle: InsertField
articleTitle: InsertField
second_title: Aspose.Words for .NET
description: DocumentBuilder InsertField yöntem. Belgeye bir Word alanı ekler ve isteğe bağlı olarak alan sonucunu günceller C#'da.
type: docs
weight: 320
url: /tr/net/aspose.words/documentbuilder/insertfield/
---
## InsertField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool*) {#insertfield}

Belgeye bir Word alanı ekler ve isteğe bağlı olarak alan sonucunu günceller.

```csharp
public Field InsertField(FieldType fieldType, bool updateField)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldType | FieldType | Eklenecek alanın türü. |
| updateField | Boolean | Alanın hemen güncellenip güncellenmeyeceğini belirtir. |

### Geri dönüş değeri

A[`Field`](../../../aspose.words.fields/field/) eklenen alanı temsil eden nesne.

## Notlar

Bu yöntem bir belgeye alan ekler. Aspose.Words çoğu türdeki alanları güncelleyebilir, ancak hepsini güncelleyemez. Daha fazla ayrıntı için the 'ye bakın`InsertField` aşırı yükleme.

## Örnekler

FieldType kullanılarak bir belgeye nasıl alan ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Oluşturucu ekledikçe güncellenip güncellenmeyeceğini belirleyen bir bayrağı geçerken iki alan ekleyin.
// Bazı durumlarda alanların güncellenmesi hesaplama açısından pahalı olabilir ve güncellemeyi ertelemek iyi bir fikir olabilir.
doc.BuiltInDocumentProperties.Author = "John Doe";
builder.Write("This document was written by ");
builder.InsertField(FieldType.FieldAuthor, updateInsertedFieldsImmediately);

builder.InsertParagraph();
builder.Write("\nThis is page ");
builder.InsertField(FieldType.FieldPage, updateInsertedFieldsImmediately);

Assert.AreEqual(" AUTHOR ", doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(" PAGE ", doc.Range.Fields[1].GetFieldCode());

if (updateInsertedFieldsImmediately)
{
    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);
    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
else
{
    Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
    Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

    // Bu alanları güncelleme yöntemlerini kullanarak manuel olarak güncellememiz gerekecek.
    doc.Range.Fields[0].Update();

    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);

    doc.UpdateFields();

    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
```

### Ayrıca bakınız

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertField(*string*) {#insertfield_1}

Belgeye bir Word alanı ekler ve alan sonucunu günceller.

```csharp
public Field InsertField(string fieldCode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldCode | String | Eklenecek alan kodu (küme parantezleri olmadan). |

### Geri dönüş değeri

A[`Field`](../../../aspose.words.fields/field/) eklenen alanı temsil eden nesne.

## Notlar

Bu yöntem bir belgeye alan ekler ve alan sonucunu hemen günceller. Aspose.Words çoğu türdeki alanları güncelleyebilir, ancak hepsini güncelleyemez. Daha fazla ayrıntı için the 'ye bakın`InsertField` aşırı yükleme.

## Örnekler

Alan kodu kullanarak belgeye nasıl alan ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// InsertField yönteminin bu aşırı yüklemesi, eklenen alanları otomatik olarak günceller.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

Alanların nasıl ekleneceğini ve belge oluşturucunun imlecinin bu alanlara nasıl taşınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// İmleci ilk MERGEFIELD'a taşıyın.
builder.MoveToMergeField("MyMergeField1", true, false);

// İmlecin ilk MERGEFIELD'den hemen sonra ve ikinciden önce yerleştirildiğine dikkat edin.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// Alanın alan kodunu veya içeriğini oluşturucuyu kullanarak düzenlemek istiyorsak,
// imlecinin bir alanın içinde olması gerekir.
// Bunu bir alanın içine yerleştirmek için belge oluşturucunun MoveTo yöntemini çağırmamız gerekir
// ve alanın başlangıç veya ayırıcı düğümünü argüman olarak iletin.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### Ayrıca bakınız

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertField(*string, string*) {#insertfield_2}

Alan sonucunu güncellemeden belgeye bir Word alanı ekler.

```csharp
public Field InsertField(string fieldCode, string fieldValue)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldCode | String | Eklenecek alan kodu (küme parantezleri olmadan). |
| fieldValue | String | Eklenecek alan değeri. Geçmek`hükümsüz` değeri olmayan alanlar için. |

### Geri dönüş değeri

A[`Field`](../../../aspose.words.fields/field/) eklenen alanı temsil eden nesne.

## Notlar

Microsoft Word belgelerindeki alanlar, alan kodu ve alan sonucundan oluşur. Alan kodu bir formül gibidir ve alan sonucu, formülün ürettiği that değeri gibidir. Alan kodu ayrıca, belirli bir eylemi gerçekleştirmek için ek talimatlara benzeyen switch alanını da içerebilir.

Alt+F9 klavye kısayolunu kullanarak Microsoft Word'de belgenizde alan kodlarını ve sonuçları görüntülemek arasında geçiş yapabilirsiniz. Alan kodları küme parantezleri ({ }) arasında görünür.

Bir alan oluşturmak için bir alan türü, alan kodu ve bir "yer tutucu" alan değeri belirtmeniz gerekir. Belirli bir alan kodu sözdiziminden emin değilseniz, alanı Microsoft Word'de öncelikle oluşturun ve alan kodunu görmek için geçiş yapın .

Aspose.Words çoğu alan türü için alan sonuçlarını hesaplayabilir ancak bu method alan sonucunu otomatik olarak güncellemez. Alan sonucu otomatik olarak hesaplanmadığından, alan sonucuna eklenecek bir dize değeri (hatta boş bir dize) iletmeniz beklenir. Bu değer, alan oluşturulana kadar yer tutucu olarak alan sonucunda kalacaktır. güncellendi. Alan sonucunu güncellemek için arayabilirsiniz[`Update`](../../../aspose.words.fields/field/update/)size döndürülen alan nesnesinde veya[`UpdateFields`](../../document/updatefields/) Tüm belgedeki alanları güncellemek için.

## Örnekler

Bir bölümde sayfa numaralandırmanın nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 3.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("Section 2, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 3.");

// Belge oluşturucuyu ilk bölümün birincil başlığına taşıyın,
// o bölümdeki her sayfanın görüntüleneceği.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// Geçerli sayfanın numarasını görüntüleyecek bir PAGE alanı ekleyin.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// PAGE alanlarının görüntülediği sayfa sayısının 5'ten başlamasını sağlayacak şekilde bölümü yapılandırın.
// Ayrıca, tüm PAGE alanlarını sayfa numaralarını büyük harf Romen rakamları kullanarak gösterecek şekilde yapılandırın.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// İkinci bölüm için başka bir PAGE alanıyla başka bir birincil başlık oluşturun.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// PAGE alanlarının görüntülediği sayfa sayısının 10'dan başlamasını sağlayacak şekilde bölümü yapılandırın.
// Ayrıca, tüm PAGE alanlarını Arapça sayıları kullanarak sayfa numaralarını gösterecek şekilde yapılandırın.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### Ayrıca bakınız

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
