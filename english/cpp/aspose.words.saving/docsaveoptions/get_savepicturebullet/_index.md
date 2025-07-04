---
title: Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet method
linktitle: get_SavePictureBullet
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet method. When false, PictureBullet data is not saved to output document. Default value is true in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.saving/docsaveoptions/get_savepicturebullet/
---
## DocSaveOptions::get_SavePictureBullet method


When **false**, PictureBullet data is not saved to output document. Default value is **true**.

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet() const
```

## Remarks


This option is provided for Word 97, which cannot work correctly with PictureBullet data. To remove PictureBullet data, set the option to "false".

## Examples



Shows how to omit PictureBullet data from the document when saving. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Image bullet points.docx");

// Some word processors, such as Microsoft Word 97, are incompatible with PictureBullet data.
// By setting a flag in the SaveOptions object,
// we can convert all image bullet points to ordinary bullet points while saving.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>(Aspose::Words::SaveFormat::Doc);
saveOptions->set_SavePictureBullet(false);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.PictureBullets.doc", saveOptions);
```

## See Also

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
