---
title: FieldHyperlink.Target
second_title: Aspose.Words for .NET API Referansı
description: FieldHyperlink mülk. Bağlantının yönlendirileceği hedefi alır veya ayarlar.
type: docs
weight: 70
url: /tr/net/aspose.words.fields/fieldhyperlink/target/
---
## FieldHyperlink.Target property

Bağlantının yönlendirileceği hedefi alır veya ayarlar.

```csharp
public string Target { get; set; }
```

### Örnekler

Yerel dosya sistemindeki belgelere bağlanmak için KÖPRÜ alanlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// Microsoft Word'de bu KÖPRÜ alanına tıkladığımızda,
// bağlantılı belgeyi açacak ve ardından imleci belirtilen yer işaretine yerleştirecek.
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// Microsoft Word'de bu KÖPRÜ alanına tıkladığımızda,
// bağlantılı belgeyi açacak ve otomatik olarak belirtilen iframe'e inecek.
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
* ad alanı [Aspose.Words.Fields](../../fieldhyperlink/)
* toplantı [Aspose.Words](../../../)


