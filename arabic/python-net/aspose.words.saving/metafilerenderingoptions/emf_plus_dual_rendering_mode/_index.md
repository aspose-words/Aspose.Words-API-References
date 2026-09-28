---
title: MetafileRenderingOptions.emf_plus_dual_rendering_mode property
linktitle: emf_plus_dual_rendering_mode property
articleTitle: emf_plus_dual_rendering_mode property
second_title: Aspose.Words for Python
description: "MetafileRenderingOptions.emf_plus_dual_rendering_mode property. Gets or sets a value determining how EMF+ Dual metafiles should be rendered."
type: docs
weight: 20
url: /ar/python-net/aspose.words.saving/metafilerenderingoptions/emf_plus_dual_rendering_mode/
---

## MetafileRenderingOptions.emf_plus_dual_rendering_mode property

Gets or sets a value determining how EMF+ Dual metafiles should be rendered.


```python
@property
def emf_plus_dual_rendering_mode(self) -> aspose.words.saving.EmfPlusDualRenderingMode:
    ...

@emf_plus_dual_rendering_mode.setter
def emf_plus_dual_rendering_mode(self, value: aspose.words.saving.EmfPlusDualRenderingMode):
    ...

```

### Remarks

EMF+ Dual metafiles contains both EMF+ and EMF parts. MS Word and GDI+ always renders EMF+ part.
Aspose.Words currently doesn't fully supports all EMF+ records and in some cases rendering result of
EMF part looks better then rendering result of EMF+ part.

This option is used only when metafile is rendered as vector graphics. When metafile is rendered
to bitmap, EMF+ part is always used.

The default value is [EmfPlusDualRenderingMode.EMF_PLUS_WITH_FALLBACK](../../emfplusdualrenderingmode/#EMF_PLUS_WITH_FALLBACK).




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

* module [aspose.words.saving](../../)
* class [MetafileRenderingOptions](../)

