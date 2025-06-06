---
title: StructuredDocumentTag
linktitle: StructuredDocumentTag
articleTitle: StructuredDocumentTag
second_title: .NET için Aspose.Words
description: StructuredDocumentTag oluşturucusu ile güçlü yapılandırılmış belgeleri zahmetsizce oluşturun. Gelişmiş organizasyon ve netlik için yeni örnekleri başlatın.
type: docs
weight: 10
url: /tr/net/aspose.words.markup/structureddocumenttag/structureddocumenttag/
---
## StructuredDocumentTag constructor

Yeni bir örneğini başlatır**Yapılandırılmış belge etiketi** sınıf.

```csharp
public StructuredDocumentTag(DocumentBase doc, SdtType type, MarkupLevel level)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | DocumentBase | Sahip belgesi. |
| type | SdtType | SDT düğümünün türü. |
| level | MarkupLevel | Belge içindeki SDT düğümünün düzeyi. |

## Notlar

Aşağıdaki SDT türleri oluşturulabilir:

* Checkbox
* DropDownList
* ComboBox
* Date
* BuildingBlockGallery
* Group
* Picture
* RichText
* PlainText

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

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [SdtType](../../sdttype/)
* enum [MarkupLevel](../../markuplevel/)
* class [StructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
