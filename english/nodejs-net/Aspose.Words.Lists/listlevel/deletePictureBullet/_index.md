---
title: ListLevel.deletePictureBullet method
linktitle: deletePictureBullet method
articleTitle: deletePictureBullet method
second_title: Aspose.Words for NodeJs
description: "ListLevel.deletePictureBullet method. Deletes picture bullet for the current list level."
type: docs
weight: 160
url: /nodejs-net/aspose.words.lists/listlevel/deletePictureBullet/
---

## deletePictureBullet() {#default}

Deletes picture bullet for the current list level.


```js
deletePictureBullet()
```

### Remarks

Default bullet will be shown after deleting.


### Examples

Shows how to set a custom image icon for list item labels.

```js
let doc = new aw.Document();

let list = doc.lists.add(aw.Lists.ListTemplate.BulletCircle);

// Create a picture bullet for the current list level, and set an image from a local file system
// as the icon that the bullets for this list level will display.
list.listLevels.at(0).createPictureBullet();
list.listLevels.at(0).imageData.setImage(base.imageDir + "Logo icon.ico");

expect(list.listLevels.at(0).imageData.hasImage).toEqual(true);

let builder = new aw.DocumentBuilder(doc);

builder.listFormat.list = list;
builder.writeln("Hello world!");
builder.write("Hello again!");

doc.save(base.artifactsDir + "Lists.createPictureBullet.docx");

list.listLevels.at(0).deletePictureBullet();

expect(list.listLevels.at(0).imageData).toBe(null);
```

### See Also

* module [Aspose.Words.Lists](../../)
* class [ListLevel](../)

