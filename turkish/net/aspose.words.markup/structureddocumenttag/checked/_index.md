---
title: StructuredDocumentTag.Checked
linktitle: Checked
articleTitle: Checked
second_title: .NET için Aspose.Words
description: Checkbox SDT'yi StructuredDocumentTag Checked özelliğiyle yönetin. Durumunu kolayca alın/ayarlayın—varsayılanı false'tur. Bugün belge etkileşimini geliştirin!
type: docs
weight: 60
url: /tr/net/aspose.words.markup/structureddocumenttag/checked/
---
## StructuredDocumentTag.Checked property

Onay Kutusunun geçerli durumunu alır/ayarlar**SDT** . Bu özelliğin varsayılan değeri:`YANLIŞ` .

```csharp
public bool Checked { get; set; }
```

## Notlar

Bu özelliğe erişim yalnızca şu amaçlar için çalışacaktır:Checkbox SDT türleri.

Diğer tüm SDT tipleri için istisna oluşacaktır.

## Örnekler

Onay kutusu biçiminde yapılandırılmış bir belge etiketinin nasıl oluşturulacağını gösterin.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

StructuredDocumentTag sdtCheckBox =
    new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline) { Checked = true };

// Bir onay kutusu içerik kontrolünün işaretli/işaretsiz durumunu temsil etmek için kullanılan sembolleri ayarlayabiliriz.
sdtCheckBox.SetCheckedSymbol(0x00A9, "Times New Roman");
sdtCheckBox.SetUncheckedSymbol(0x00AE, "Times New Roman");

builder.InsertNode(sdtCheckBox);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CheckBox.docx");
```

### Ayrıca bakınız

* class [StructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
