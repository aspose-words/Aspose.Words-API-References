---
title: EmfPlusDualRenderingMode enumeration
linktitle: EmfPlusDualRenderingMode enumeration
articleTitle: EmfPlusDualRenderingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.EmfPlusDualRenderingMode enumeration. Specifies how Aspose.Words should render EMF+ Dual metafiles."
type: docs
weight: 160
url: /ar/python-net/aspose.words.saving/emfplusdualrenderingmode/
---

## EmfPlusDualRenderingMode enumeration

Specifies how Aspose.Words should render EMF+ Dual metafiles.


### Members

| Name | Description |
| --- | --- |
| EMF_PLUS_WITH_FALLBACK | Aspose.Words tries to render EMF+ part of EMF+ Dual metafile. If some of the EMF+ records are not supported then Aspose.Words renders EMF part of EMF+ Dual metafile. |
| EMF_PLUS | Aspose.Words renders EMF+ part of EMF+ Dual metafile. |
| EMF | Aspose.Words renders EMF part of EMF+ Dual metafile. |

### Examples

Shows how to configure Enhanced Windows Metafile-related rendering options when saving to PDF.

```python
doc = aw.Document(file_name=MY_DIR + 'EMF.docx')
# أنشئ كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .PDF.
save_options = aw.saving.PdfSaveOptions()
# قم بتعيين الخاصية "EmfPlusDualRenderingMode" إلى "EmfPlusDualRenderingMode.Emf"
# لإظهار الجزء EMF فقط من ملف تعريف EMF+ المزدوج.
# قم بتعيين الخاصية "EmfPlusDualRenderingMode" إلى "EmfPlusDualRenderingMode.EmfPlus" لت
# لإظهار الجزء EMF+ من ملف تعريف EMF+ المزدوج.
# قم بتعيين الخاصية "EmfPlusDualRenderingMode" إلى "EmfPlusDualRenderingMode.EmfPlusWithFallback"
# لإظهار الجزء EMF+ من ملف تعريف EMF+ المزدوج إذا كانت جميع سجلات EMF+ مدعومة.
# إلا، سيقوم Aspose.Words بعرض الجزء EMF.
save_options.metafile_rendering_options.emf_plus_dual_rendering_mode = rendering_mode
# قم بتعيين الخاصية "UseEmfEmbeddedToWmf" إلى "true" لعرض بيانات EMF المدمجة
# لملفات التعريف التي يمكننا عرضها كرسومات متجهة.
save_options.metafile_rendering_options.use_emf_embedded_to_wmf = True
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.RenderMetafile.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

