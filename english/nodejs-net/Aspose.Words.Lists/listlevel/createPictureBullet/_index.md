---
title: ListLevel.createPictureBullet method
linktitle: createPictureBullet method
articleTitle: createPictureBullet method
second_title: Aspose.Words for Node.js
description: "ListLevel.createPictureBullet method. Creates picture bullet shape for the current list level."
type: docs
weight: 150
url: /nodejs-net/aspose.words.lists/listlevel/createPictureBullet/
---

## createPictureBullet() {#default}

Creates picture bullet shape for the current list level.


```js
createPictureBullet()
```

### Remarks

Please note, [ListLevel.numberStyle](../numberStyle/) will be set to [NumberStyle.Bullet](../../../aspose.words/numberstyle/#Bullet) and
[ListLevel.numberFormat](../numberFormat/) to "\\xF0B7" to properly display picture bullet.
Red cross image will be set as picture bullet image upon creating.
To change it please use [ListLevel.imageData](../imageData/).


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

