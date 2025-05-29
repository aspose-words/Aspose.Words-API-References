---
title: DocumentBuilder.InsertField
linktitle: InsertField
articleTitle: InsertField
second_title: .NET için Aspose.Words
description: Belgelerinizi DocumentBuilder'ın InsertField yöntemiyle geliştirin. Dinamik içerik ve gelişmiş işlevsellik için Word alanlarını zahmetsizce ekleyin ve güncelleyin.
type: docs
weight: 330
url: /tr/net/aspose.words/documentbuilder/insertfield/
---
## InsertField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool*) {#insertfield}

Bir Word alanını bir belgeye ekler ve isteğe bağlı olarak alan sonucunu günceller.

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

Bu yöntem bir belgeye bir alan ekler. Aspose.Words çoğu türün alanlarını güncelleyebilir, ancak hepsini değil. Daha fazla ayrıntı için bkz. `InsertField` aşırı yük.

## Örnekler

FieldType kullanılarak bir belgeye alanın nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Oluşturucu eklerken güncellenip güncellenmeyeceğini belirleyen bir bayrak geçirerek iki alan ekleyin.
// Bazı durumlarda, alanların güncellenmesi hesaplama açısından maliyetli olabilir ve güncellemeyi ertelemek iyi bir fikir olabilir.
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

    // Bu alanları güncelleme yöntemlerini kullanarak manuel olarak güncellememiz gerekecektir.
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

Bir Word alanını bir belgeye ekler ve alan sonucunu günceller.

```csharp
public Field InsertField(string fieldCode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldCode | String | Eklenecek alan kodu (süslü parantez olmadan). |

### Geri dönüş değeri

A[`Field`](../../../aspose.words.fields/field/) eklenen alanı temsil eden nesne.

## Notlar

Bu yöntem bir belgeye bir alan ekler ve alan sonucunu hemen günceller. Aspose.Words çoğu türün alanlarını güncelleyebilir, ancak hepsini değil. Daha fazla ayrıntı için bkz. `InsertField` aşırı yük.

## Örnekler

Alan kodu kullanılarak bir belgeye alanın nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// InsertField yönteminin bu aşırı yüklemesi eklenen alanları otomatik olarak günceller.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

Alanların nasıl ekleneceğini ve belge oluşturucunun imlecinin bunlara nasıl taşınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// İmleci ilk MERGEFIELD'a taşı.
builder.MoveToMergeField("MyMergeField1", true, false);

// İmlecin ilk MERGEFIELD'dan hemen sonra, ikinciden ise önce yerleştirildiğine dikkat edin.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// Alanın alan kodunu veya içeriğini oluşturucuyu kullanarak düzenlemek istersek,
// imlecinin bir alanın içerisinde olması gerekir.
// Bunu bir alanın içine yerleştirmek için, belge oluşturucunun MoveTo yöntemini çağırmamız gerekir
// ve alanın başlangıç veya ayırıcı düğümünü argüman olarak geçirin.
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

Alan sonucunu güncellemeden bir Word alanını belgeye ekler.

```csharp
public Field InsertField(string fieldCode, string fieldValue)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldCode | String | Eklenecek alan kodu (süslü parantez olmadan). |
| fieldValue | String | Eklenecek alan değeri. Geç`hükümsüz` değeri olmayan alanlar için. |

### Geri dönüş değeri

A[`Field`](../../../aspose.words.fields/field/) eklenen alanı temsil eden nesne.

## Notlar

Microsoft Word belgelerindeki alanlar bir alan kodu ve bir alan sonucundan oluşur. Alan kodu bir formül gibidir ve alan sonucu formülün ürettiği değere benzer. Alan kodu ayrıca belirli bir eylemi gerçekleştirmek için ek talimatlar gibi olan alan anahtarları içerebilir.

Belgenizde alan kodlarını ve sonuçları görüntülemek arasında geçiş yapmak için Alt+F9 klavye kısayolunu kullanabilirsiniz. Alan kodları süslü parantezler ( { } ) arasında görünür.

Bir alan oluşturmak için, bir alan türü, alan kodu ve bir "yer tutucu" alan değeri belirtmeniz gerekir. Belirli bir alan kodu sözdiziminden emin değilseniz, önce Microsoft Word'de alanı oluşturun ve alan kodunu görmek için geçiş yapın.

Aspose.Words, alan türlerinin çoğu için alan sonuçlarını hesaplayabilir, ancak bu method alan sonucunu otomatik olarak güncellemez. Alan sonucu otomatik olarak hesaplanmadığından, alan sonucuna eklenecek bir dize değeri (veya boş bir dize) geçirmeniz beklenir. Bu değer, alan güncellenene kadar alan sonucunda yer tutucu olarak kalacaktır. Alan sonucunu güncellemek için şunu çağırabilirsiniz:[`Update`](../../../aspose.words.fields/field/update/) alan nesnesi üzerinde size veya return [`UpdateFields`](../../document/updatefields/) tüm belgedeki alanları güncellemek için.

## Örnekler

Bir bölümde sayfa numaralandırmasının nasıl ayarlanacağını gösterir.

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
// bu bölümdeki her sayfanın görüntüleyeceği.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// Mevcut sayfanın numarasını gösterecek bir SAYFA alanı ekleyin.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// SAYFA alanlarının görüntülediği sayfa sayısının 5'ten başlamasını sağlayacak şekilde bölümü yapılandırın.
// Ayrıca, tüm SAYFA alanlarını sayfa numaralarını büyük harfli Roma rakamları kullanarak görüntüleyecek şekilde yapılandırın.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// İkinci bölüm için başka bir SAYFA alanı içeren başka bir birincil başlık oluşturun.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// SAYFA alanlarının görüntülediği sayfa sayısının 10'dan başlaması için bölümü yapılandırın.
// Ayrıca tüm PAGE alanlarını sayfa numaralarını Arap rakamları kullanarak görüntüleyecek şekilde yapılandırın.
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
