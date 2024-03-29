---
title: StructuredDocumentTag.SetCheckedSymbol
linktitle: SetCheckedSymbol
articleTitle: SetCheckedSymbol
second_title: Aspose.Words for .NET
description: StructuredDocumentTag SetCheckedSymbol yöntem. Onay kutusu içerik denetiminin işaretli durumunu temsil etmek için kullanılan sembolü ayarlar C#'da.
type: docs
weight: 360
url: /tr/net/aspose.words.markup/structureddocumenttag/setcheckedsymbol/
---
## StructuredDocumentTag.SetCheckedSymbol method

Onay kutusu içerik denetiminin işaretli durumunu temsil etmek için kullanılan sembolü ayarlar.

```csharp
public void SetCheckedSymbol(int characterCode, string fontName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| characterCode | Int32 | Belirtilen sembolün karakter kodu. |
| fontName | String | Sembolü içeren yazı tipinin adı. |

## Notlar

Bu yönteme erişim yalnızca aşağıdakiler için işe yarayacaktır:Checkbox SDT türleri.

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
