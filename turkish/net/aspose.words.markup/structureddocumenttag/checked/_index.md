---
title: StructuredDocumentTag.Checked
linktitle: Checked
articleTitle: Checked
second_title: Aspose.Words for .NET
description: StructuredDocumentTag Checked mülk. Onay Kutusunun geçerli durumunu alır/ayarlarSDT . Bu özelliğin varsayılan değeriYANLIŞ  C#'da.
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

Bu özelliğe erişim yalnızca şunun için işe yarayacaktır:Checkbox SDT türleri.

Diğer tüm SDT türleri için istisna meydana gelecektir.

## Örnekler

Onay kutusu biçiminde yapılandırılmış belge etiketinin nasıl oluşturulacağını gösterin.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

StructuredDocumentTag sdtCheckBox =
    new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline) {Checked = true};

// Onay kutusu içerik kontrolünün işaretli/işaretsiz durumunu temsil etmek için kullanılan sembolleri ayarlayabiliriz.
sdtCheckBox.SetCheckedSymbol(0x00A9, "Times New Roman");
sdtCheckBox.SetUncheckedSymbol(0x00AE, "Times New Roman");

builder.InsertNode(sdtCheckBox);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CheckBox.docx");
```

### Ayrıca bakınız

* class [StructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
