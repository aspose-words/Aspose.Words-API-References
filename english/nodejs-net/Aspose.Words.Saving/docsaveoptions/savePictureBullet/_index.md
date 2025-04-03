---
title: DocSaveOptions.savePictureBullet property
linktitle: savePictureBullet property
articleTitle: savePictureBullet property
second_title: Aspose.Words for NodeJs
description: "DocSaveOptions.savePictureBullet property. When ``false``, PictureBullet data is not saved to output document"
type: docs
weight: 60
url: /nodejs-net/Aspose.Words.Saving/docsaveoptions/savePictureBullet/
---

## DocSaveOptions.savePictureBullet property

When ``false``, PictureBullet data is not saved to output document.
Default value is ``true``.



```js
get savePictureBullet(): boolean
```

### Remarks

This option is provided for Word 97, which cannot work correctly with PictureBullet data.
To remove PictureBullet data, set the option to "false".




### Examples

Shows how to omit PictureBullet data from the document when saving.

```js
let doc = new aw.Document(base.myDir + "Image bullet points.docx");
expect(doc.lists.at(0).listLevels.at(0).imageData).not.toBe(null);

// Some word processors, such as Microsoft Word 97, are incompatible with PictureBullet data.
// By setting a flag in the SaveOptions object,
// we can convert all image bullet points to ordinary bullet points while saving.
let saveOptions = new aw.Saving.DocSaveOptions(aw.SaveFormat.Doc);
saveOptions.savePictureBullet = false;

doc.save(base.artifactsDir + "DocSaveOptions.PictureBullets.doc", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [DocSaveOptions](../)

