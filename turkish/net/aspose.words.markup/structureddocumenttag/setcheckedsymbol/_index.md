---
title: StructuredDocumentTag.SetCheckedSymbol
linktitle: SetCheckedSymbol
articleTitle: SetCheckedSymbol
second_title: .NET için Aspose.Words
description: Onay kutusu görsellerini özelleştirmek ve kullanıcı deneyimini geliştirmek için StructuredDocumentTag'de SetCheckedSymbol yönteminin nasıl kullanılacağını keşfedin.
type: docs
weight: 380
url: /tr/net/aspose.words.markup/structureddocumenttag/setcheckedsymbol/
---
## StructuredDocumentTag.SetCheckedSymbol method

Bir onay kutusu içerik denetiminin işaretli durumunu temsil etmek için kullanılan simgeyi ayarlar.

```csharp
public void SetCheckedSymbol(int characterCode, string fontName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| characterCode | Int32 | Belirtilen sembol için karakter kodu. |
| fontName | String | Sembolü içeren yazı tipinin adı. |

## Notlar

Bu yönteme erişim yalnızca şu amaçlar için işe yarayacaktır:Checkbox SDT tipleri.

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
