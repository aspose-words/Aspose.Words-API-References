---
title: PdfSaveOptions.RenderChoiceFormFieldBorder
linktitle: RenderChoiceFormFieldBorder
articleTitle: RenderChoiceFormFieldBorder
second_title: .NET için Aspose.Words
description: PdfSaveOptions RenderChoiceFormFieldBorder özelliğinin, daha iyi kullanıcı deneyimi için seçim alanı kenarlıklarını kontrol ederek PDF form tasarımını nasıl geliştirdiğini keşfedin.
type: docs
weight: 290
url: /tr/net/aspose.words.saving/pdfsaveoptions/renderchoiceformfieldborder/
---
## PdfSaveOptions.RenderChoiceFormFieldBorder property

PDF seçim formu alanı kenarlığının işlenip işlenmeyeceğini belirtir.

```csharp
public bool RenderChoiceFormFieldBorder { get; set; }
```

## Notlar

PDF seçim form alanları, SDT Combo Box İçerik Denetimi, SDT Açılır Liste İçeriği Denetimi ve eski Açılır Form Alanının dışa aktarılması için kullanılır.[`PreserveFormFields`](../preserveformfields/) seçeneği etkinleştirildi.

Varsayılan değer:`doğru`.

## Örnekler

PDF seçim formu alan sınırının nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Legacy drop-down.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PreserveFormFields = true;
saveOptions.RenderChoiceFormFieldBorder = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderChoiceFormFieldBorder.pdf", saveOptions);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
