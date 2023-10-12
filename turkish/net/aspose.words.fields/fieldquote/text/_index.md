---
title: FieldQuote.Text
second_title: Aspose.Words for .NET API Referansı
description: FieldQuote mülk. Alınacak metni alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldquote/text/
---
## FieldQuote.Text property

Alınacak metni alır veya ayarlar.

```csharp
public string Text { get; set; }
```

### Örnekler

QUOTE alanının kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Text özelliğinin değerini gösterecek bir QUOTE alanı ekleyin.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Bir QUOTE alanı ekleyin ve içine bir DATE alanı yerleştirin.
// DATE alanları, belgeyi Microsoft Word kullanarak her açtığımızda değerlerini geçerli tarihe günceller.
// DATE alanını QUOTE alanının içine bu şekilde yerleştirmek, değerini donduracaktır
// belgeyi oluşturduğumuz tarihe.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Doğru sonuçları görüntülemek için tüm alanları güncelleyin.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

### Ayrıca bakınız

* class [FieldQuote](../)
* ad alanı [Aspose.Words.Fields](../../fieldquote/)
* toplantı [Aspose.Words](../../../)


