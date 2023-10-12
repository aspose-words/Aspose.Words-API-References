---
title: FieldGoToButton.Location
second_title: Aspose.Words for .NET API Referansı
description: FieldGoToButton mülk. Bir yer iminin sayfa numarasının veya atlanacak başka bir öğenin adını alır veya ayarlar.
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldgotobutton/location/
---
## FieldGoToButton.Location property

Bir yer iminin, sayfa numarasının veya atlanacak başka bir öğenin adını alır veya ayarlar.

```csharp
public string Location { get; set; }
```

### Örnekler

GOTOBUTTON alanı eklemeyi gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// GOTOBUTTON alanı ekleyin. Microsoft Word'de bu alana çift tıkladığımızda,
// metin imlecini Location özelliğinin ismine referans verdiği yer imine götürecektir.
FieldGoToButton field = (FieldGoToButton)builder.InsertField(FieldType.FieldGoToButton, true);
field.DisplayText = "My Button";
field.Location = "MyBookmark";

Assert.AreEqual(" GOTOBUTTON  MyBookmark My Button", field.GetFieldCode());

// Referans verilecek alan için geçerli bir yer imi ekleyin.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark(field.Location);
builder.Writeln("Bookmark text contents.");
builder.EndBookmark(field.Location);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.GOTOBUTTON.docx");
```

### Ayrıca bakınız

* class [FieldGoToButton](../)
* ad alanı [Aspose.Words.Fields](../../fieldgotobutton/)
* toplantı [Aspose.Words](../../../)


