---
title: get_SavePictureBullet
second_title: Aspose.Words for C++ API Reference
description: When false, PictureBullet data is not saved to output document. Default value is true.
type: docs
weight: 53
url: /cpp/aspose.words.saving/docsaveoptions/get_savepicturebullet/
---
## DocSaveOptions.get_SavePictureBullet method


When **false**, PictureBullet data is not saved to output document. Default value is **true**.

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet() const
```


This option is provided for Word 97, which cannot work correctly with PictureBullet data. To remove PictureBullet data, set the option to "false".

## Examples




Shows how to omit PictureBullet data from the document when saving. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Image bullet points.docx");

// Some word processors, such as Microsoft Word 97, are incompatible with PictureBullet data.
// By setting a flag in the SaveOptions object,
// we can convert all image bullet points to ordinary bullet points while saving.
auto saveOptions = MakeObject<DocSaveOptions>(SaveFormat::Doc);
saveOptions->set_SavePictureBullet(false);

doc->Save(ArtifactsDir + u"DocSaveOptions.PictureBullets.doc", saveOptions);
```

