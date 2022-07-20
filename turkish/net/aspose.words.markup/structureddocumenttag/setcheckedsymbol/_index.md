---
title: SetCheckedSymbol
second_title: Aspose.Words for .NET API Referansı
description: Bir onay kutusu içerik denetiminin işaretli durumunu temsil etmek için kullanılan sembolü ayarlar.
type: docs
weight: 350
url: /tr/net/aspose.words.markup/structureddocumenttag/setcheckedsymbol/
---
## StructuredDocumentTag.SetCheckedSymbol method

Bir onay kutusu içerik denetiminin işaretli durumunu temsil etmek için kullanılan sembolü ayarlar.

```csharp
public void SetCheckedSymbol(int characterCode, string fontName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| characterCode | Int32 | Belirtilen sembol için karakter kodu. |
| fontName | String | Sembolü içeren yazı tipinin adı. |

### Notlar

Bu yönteme erişmek yalnızcaCheckbox SDT türleri.

Diğer tüm SDT türleri için istisna oluşacaktır.

### Örnekler

Onay kutusu şeklinde yapılandırılmış bir belge etiketinin nasıl oluşturulacağını gösterin.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

StructuredDocumentTag sdtCheckBox =
    new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline) {Checked = true};

// Bir onay kutusu içerik kontrolünün işaretli/işaretsiz durumunu temsil etmek için kullanılan sembolleri ayarlayabiliriz.
sdtCheckBox.SetCheckedSymbol(0x00A9, "Times New Roman");
sdtCheckBox.SetUncheckedSymbol(0x00AE, "Times New Roman");

builder.InsertNode(sdtCheckBox);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CheckBox.docx");
```

### Ayrıca bakınız

* class [StructuredDocumentTag](../../structureddocumenttag)
* ad alanı [Aspose.Words.Markup](../../structureddocumenttag)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->