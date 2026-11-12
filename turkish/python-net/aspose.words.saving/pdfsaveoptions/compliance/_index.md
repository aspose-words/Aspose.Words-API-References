---
title: PdfSaveOptions.compliance property
linktitle: compliance property
articleTitle: compliance property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.compliance property. Specifies the PDF standards compliance level for output documents."
type: docs
weight: 50
url: /tr/python-net/aspose.words.saving/pdfsaveoptions/compliance/
---

## PdfSaveOptions.compliance property

Specifies the PDF standards compliance level for output documents.


```python
@property
def compliance(self) -> aspose.words.saving.PdfCompliance:
    ...

@compliance.setter
def compliance(self, value: aspose.words.saving.PdfCompliance):
    ...

```

### Remarks

Default is [PdfCompliance.PDF17](../../pdfcompliance/#PDF17).




### Examples

Shows how to set the PDF standards compliance level of saved PDF documents.

```python
doc = aw.Document(file_name=MY_DIR + 'Images.docx')
# "PdfSaveOptions" nesnesi oluşturun; bu nesneyi belgenin "Save" metoduna geçebiliriz
# bu yöntemin belgeyi .PDF'ye nasıl dönüştürdüğünü değiştirmek için.
# Bazı PdfSaveOptions'ların standartlardan birine kaydederken yasaklandığını ve otomatik olarak düzeltildiğini unutmayın.
# Hangi seçeneklerin otomatik olarak düzeltildiğini öğrenmek için IWarningCallback kullanın.
save_options = aw.saving.PdfSaveOptions()
# "Compliance" özelliğini "PdfCompliance.PdfA1b" olarak ayarlayarak "PDF/A-1b" standardına uyun,
# bu, Aspose.Words'ün belgeyi PDF'ye dönüştürürken görsel görünümünü korumayı amaçlar.
# "Compliance" özelliğini "PdfCompliance.Pdf17" olarak ayarlayarak "1.7" standardına uyun.
# "Compliance" özelliğini "PdfCompliance.PdfA1a" olarak ayarlayın, "PDF/A-1a" standardına uymak için,
# "PDF/A-1b" standardına da uyar ve orijinal belgenin belge yapısını korur.
# "Compliance" özelliğini "PdfCompliance.PdfUa1" olarak ayarlayın, "PDF/UA-1" (ISO 14289-1) standardına uymak için,
# PDF içinde elektronik belgeleri temsil etmeyi tanımlamayı amaçlar ve dosyanın erişilebilir olmasını sağlar.
# "Compliance" özelliğini "PdfCompliance.Pdf20" olarak ayarlayın, "PDF 2.0" (ISO 32000-2) standardına uymak için.
# "Compliance" özelliğini "PdfCompliance.PdfA4" olarak ayarlayın, "PDF/A-4" (ISO 19004:2020) standardına uymak için,
# belgenin statik görsel görünümünü zaman içinde korur.
# "Compliance" özelliğini "PdfCompliance.PdfA4Ua2" olarak ayarlayın, hem PDF/A-4 (ISO 19005-4:2020)
# ve PDF/UA-2 (ISO 14289-2:2024) standartlarına.
# "Compliance" özelliğini "PdfCompliance.PdfUa2" olarak ayarlayın, PDF/UA-2 (ISO 14289-2:2024) standardına uymak için.
# Bu, belgelerin aranabilir olmasını sağlar ancak zaten büyük belgelerin boyutunu önemli ölçüde artırabilir.
save_options.compliance = pdf_compliance
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.Compliance.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

