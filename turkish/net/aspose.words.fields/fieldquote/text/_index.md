---
title: FieldQuote.Text
linktitle: Text
articleTitle: Text
second_title: .NET için Aspose.Words
description: FieldQuote Metin özelliği. Gelişmiş veri yönetimi için metni kolayca alın veya ayarlayın. Bu güçlü özellik ile iş akışınızı kolaylaştırın!
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldquote/text/
---
## FieldQuote.Text property

Alınacak metni alır veya ayarlar.

```csharp
public string Text { get; set; }
```

## Örnekler

QUOTE alanının kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Text özelliğinin değerini gösterecek bir QUOTE alanı ekleyin.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Bir QUOTE alanı ekleyin ve içine bir DATE alanı yerleştirin.
// DATE alanları, Microsoft Word kullanarak belgeyi her açtığımızda değerlerini geçerli tarihe günceller.
// DATE alanını bu şekilde QUOTE alanının içine yerleştirmek değerini donduracaktır
// belgeyi oluşturduğumuz tarihe.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Tüm alanları doğru sonuçları gösterecek şekilde güncelleyin.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

### Ayrıca bakınız

* class [FieldQuote](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
