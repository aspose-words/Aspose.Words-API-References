---
title: InsertField
second_title: Aspose.Words for .NET API Referansı
description: Belgeye bir Word alanı ekler ve isteğe bağlı olarak alan sonucunu günceller.
type: docs
weight: 300
url: /tr/net/aspose.words/documentbuilder/insertfield/
---
## InsertField(FieldType, bool) {#insertfield}

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

### Notlar

Bu yöntem, bir belgeye bir alan ekler. Aspose.Words, tüm alanları değil, çoğu türü güncelleyebilir. Daha fazla ayrıntı için bkz. the [`InsertField`](./insertfield/) aşırı yükleme.

### Örnekler

FieldType kullanarak bir belgeye nasıl alan ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Oluşturucu eklerken güncellenip güncellenmeyeceğini belirleyen bir bayrak geçerken iki alan ekleyin.
// Bazı durumlarda, alanların güncellenmesi hesaplama açısından pahalı olabilir ve güncellemeyi ertelemek iyi bir fikir olabilir.
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

    // Güncelleme yöntemlerini manuel olarak kullanarak bu alanları güncellememiz gerekecek.
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
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertField(string) {#insertfield_1}

Belgeye bir Word alanı ekler ve alan sonucunu günceller.

```csharp
public Field InsertField(string fieldCode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldCode | String | Eklenecek alan kodu (kıvrımlı parantezler olmadan). |

### Geri dönüş değeri

A[`Field`](../../../aspose.words.fields/field/) eklenen alanı temsil eden nesne.

### Notlar

Bu yöntem, bir belgeye bir alan ekler ve alan sonucunu anında günceller. Aspose.Words, çoğu türün alanını güncelleyebilir, ancak hepsini değil. Daha fazla ayrıntı için bkz. the [`InsertField`](./insertfield/) aşırı yükleme.

### Örnekler

Alan kodu kullanarak bir belgeye nasıl alan ekleneceğini gösterir.

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

// İmleci ilk MERGEFIELD'e taşıyın.
builder.MoveToMergeField("MyMergeField1", true, false);

// İmlecin ilk MERGEFIELD'den hemen sonra ve ikinciden önce yerleştirildiğini unutmayın.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// Oluşturucuyu kullanarak alanın alan kodunu veya içeriğini düzenlemek istiyorsak,
// imlecinin bir alanın içinde olması gerekir.
// Bir alanın içine yerleştirmek için belge oluşturucunun MoveTo yöntemini çağırmamız gerekir
// ve alanın başlangıç veya ayırıcı düğümünü argüman olarak iletin.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### Ayrıca bakınız

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertField(string, string) {#insertfield_2}

Alan sonucunu güncellemeden belgeye bir Word alanı ekler.

```csharp
public Field InsertField(string fieldCode, string fieldValue)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldCode | String | Eklenecek alan kodu (kıvrımlı parantezler olmadan). |
| fieldValue | String | Eklenecek alan değeri. Değeri olmayan alanlar için null iletin. |

### Geri dönüş değeri

A[`Field`](../../../aspose.words.fields/field/) eklenen alanı temsil eden nesne.

### Notlar

Microsoft Word belgelerindeki alanlar, bir alan kodu ve bir alan sonucundan oluşur. Alan kodu bir formül gibidir ve alan sonucu, formülün ürettiği değeri gibidir. Alan kodu ayrıca, belirli bir eylemi gerçekleştirmek için ek talimatlara benzeyen alan anahtarları içerebilir.

Alt+F9 klavye kısayolunu kullanarak Microsoft Word'de belgenizdeki alan kodlarını ve sonuçları görüntüleme arasında geçiş yapabilirsiniz. Alan kodları küme parantezleri ( { } ) arasında görünür.

Bir alan oluşturmak için bir alan türü, alan kodu ve bir "yer tutucu" alan değeri belirtmeniz gerekir. Belirli bir alan kodu sözdiziminden emin değilseniz, alanı Microsoft Word'de oluşturun first ve alan kodunu görmek için geçiş yapın. .

Aspose.Words alan türlerinin çoğu için alan sonuçlarını hesaplayabilir, ancak bu method alan sonucunu otomatik olarak güncellemez. Alan sonucu otomatik olarak hesaplanmadığından, alan sonucuna eklenecek bazı dize değerlerini (hatta boş bir dizeyi) iletmeniz beklenir. Bu değer, alan tamamlanana kadar alan sonucunda yer tutucu olarak kalacaktır. güncellendi. Alan sonucunu güncellemek için arayabilirsiniz[`Update`](../../../aspose.words.fields/field/update/)size döndürülen alan nesnesinde veya[`UpdateFields`](../../document/updatefields/) tüm belgedeki alanları güncellemek için.

### Örnekler

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

// Geçerli sayfanın numarasını gösterecek bir SAYFA alanı ekleyin.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// Bölümü, SAYFA alanlarının gösterdiği sayfa sayısının 5'ten başlamasını sağlayacak şekilde yapılandırın.
// Ayrıca, tüm SAYFA alanlarını, büyük Romen rakamları kullanarak sayfa numaralarını gösterecek şekilde yapılandırın.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// İkinci bölüm için başka bir SAYFA alanıyla başka bir birincil başlık oluşturun.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// SAYFA alanlarının gösterdiği sayfa sayısının 10'dan başlaması için bölümü yapılandırın.
// Ayrıca, tüm SAYFA alanlarını Arapça sayıları kullanarak sayfa numaralarını gösterecek şekilde yapılandırın.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### Ayrıca bakınız

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
