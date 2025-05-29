---
title: FieldGoToButton.DisplayText
linktitle: DisplayText
articleTitle: DisplayText
second_title: .NET için Aspose.Words
description: Kullanıcı deneyimini geliştirmek için FieldGoToButton'ınızın DisplayText özelliğini özelleştirin. Sorunsuz belge gezintisi ve hızlı erişim için düğme metnini kolayca ayarlayın.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldgotobutton/displaytext/
---
## FieldGoToButton.DisplayText property

Belgede görünen "düğmenin" metnini alır veya ayarlar, böylece atlamayı etkinleştirmek için seçilebilir.

```csharp
public string DisplayText { get; set; }
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
