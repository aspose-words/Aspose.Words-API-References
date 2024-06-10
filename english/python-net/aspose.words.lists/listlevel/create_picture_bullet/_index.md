---
title: ListLevel.create_picture_bullet method
linktitle: create_picture_bullet method
articleTitle: create_picture_bullet method
second_title: Aspose.Words for Python
description: "ListLevel.create_picture_bullet method. Creates picture bullet shape for the current list level."
type: docs
weight: 150
url: /python-net/aspose.words.lists/listlevel/create_picture_bullet/
---

## create_picture_bullet() {#default}

Creates picture bullet shape for the current list level.


```python
def create_picture_bullet(self):
    ...
```

### Remarks

Please note, [ListLevel.number_style](../number_style/) will be set to [NumberStyle.BULLET](../../../aspose.words/numberstyle/#BULLET) and
[ListLevel.number_format](../number_format/) to "\\xF0B7" to properly display picture bullet.
Red cross image will be set as picture bullet image upon creating.
To change it please use [ListLevel.image_data](../image_data/).


### Examples

Shows how to set a custom image icon for list item labels.

```python
doc = aw.Document()
list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_CIRCLE)
# Create a picture bullet for the current list level, and set an image from a local file system
# as the icon that the bullets for this list level will display.
list.list_levels[0].create_picture_bullet()
list.list_levels[0].image_data.set_image(file_name=IMAGE_DIR + 'Logo icon.ico')
self.assertTrue(list.list_levels[0].image_data.has_image)
builder = aw.DocumentBuilder(doc)
builder.list_format.list = list
builder.writeln('Hello world!')
builder.write('Hello again!')
doc.save(file_name=ARTIFACTS_DIR + 'Lists.CreatePictureBullet.docx')
list.list_levels[0].delete_picture_bullet()
self.assertIsNone(list.list_levels[0].image_data)
```

### See Also

* module [aspose.words.lists](../../)
* class [ListLevel](../)

