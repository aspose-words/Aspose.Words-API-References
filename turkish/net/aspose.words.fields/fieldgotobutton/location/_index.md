---
title: FieldGoToButton.Location
linktitle: Location
articleTitle: Location
second_title: .NET için Aspose.Words
description: FieldGoToButton Location özelliğini keşfedin, sorunsuz gezinme ve gelişmiş kullanıcı deneyimi için yer imlerini, sayfa numaralarını veya öğeleri kolayca ayarlayın.
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldgotobutton/location/
---
## FieldGoToButton.Location property

Bir yer iminin, sayfa numarasının veya atlanacak başka bir öğenin adını alır veya ayarlar.

```csharp
public string Location { get; set; }
```

## Örnekler

GOTOBUTTON alanı eklemeyi gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// GOTOBUTTON alanı ekleyin. Microsoft Word'de bu alana çift tıkladığımızda,
// metin imlecini Location özelliğinin referans verdiği yer imine götürür.
FieldGoToButton field = (FieldGoToButton)builder.InsertField(FieldType.FieldGoToButton, true);
field.DisplayText = "My Button";
field.Location = "MyBookmark";

Assert.AreEqual(" GOTOBUTTON  MyBookmark My Button", field.GetFieldCode());

// Başvurulacak alan için geçerli bir yer imi ekleyin.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark(field.Location);
builder.Writeln("Bookmark text contents.");
builder.EndBookmark(field.Location);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.GOTOBUTTON.docx");
```

### Ayrıca bakınız

* class [FieldGoToButton](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
