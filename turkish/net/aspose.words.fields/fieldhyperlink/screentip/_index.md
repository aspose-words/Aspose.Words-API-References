---
title: FieldHyperlink.ScreenTip
linktitle: ScreenTip
articleTitle: ScreenTip
second_title: .NET için Aspose.Words
description: Kullanıcı deneyimini ve etkileşimi geliştirerek köprü metninizi özelleştirmek için FieldHyperlink ScreenTip özelliğini keşfedin. Bağlantılarınızı bugün optimize edin!
type: docs
weight: 50
url: /tr/net/aspose.words.fields/fieldhyperlink/screentip/
---
## FieldHyperlink.ScreenTip property

Köprü metni için Ekran İpucu metnini alır veya ayarlar.

```csharp
public string ScreenTip { get; set; }
```

## Örnekler

Yerel dosya sistemindeki belgelere bağlanmak için HYPERLINK alanlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// Microsoft Word'de bu HYPERLINK alanına tıkladığımızda,
// Bağlantılı belgeyi açacak ve ardından imleci belirtilen yer imine yerleştirecektir.
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// Microsoft Word'de bu HYPERLINK alanına tıkladığımızda,
// Bağlantılı belgeyi açacak ve otomatik olarak belirtilen iframe'e doğru kaydıracaktır.
field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);
field.Address = MyDir + "Iframes.html";
field.ScreenTip = "Open " + field.Address;
field.Target = "iframe_3";
field.OpenInNewWindow = true;
field.IsImageMap = false;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.HYPERLINK.docx");
```

### Ayrıca bakınız

* class [FieldHyperlink](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
