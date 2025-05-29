---
title: FieldHyperlink.IsImageMap
linktitle: IsImageMap
articleTitle: IsImageMap
second_title: .NET için Aspose.Words
description: FieldHyperlink IsImageMap özelliğinin, köprü metinlerine koordinatlar ekleyerek işlevselliği artırarak sunucu tarafındaki görüntü haritalarınızı nasıl geliştirdiğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldhyperlink/isimagemap/
---
## FieldHyperlink.IsImageMap property

Sunucu tarafı görüntü haritası için köprü metnine koordinatların eklenip eklenmeyeceğini alır veya ayarlar.

```csharp
public bool IsImageMap { get; set; }
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
