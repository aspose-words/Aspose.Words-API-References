---
title: ListLevel.delete_picture_bullet method
linktitle: delete_picture_bullet method
articleTitle: delete_picture_bullet method
second_title: Aspose.Words for Python
description: "ListLevel.delete_picture_bullet method. Deletes picture bullet for the current list level."
type: docs
weight: 160
url: /python-net/aspose.words.lists/listlevel/delete_picture_bullet/
---

## delete_picture_bullet() {#default}

Deletes picture bullet for the current list level.


```python
def delete_picture_bullet(self):
    ...
```

### Remarks

Default bullet will be shown after deleting.


### Examples

Shows how to set a custom image icon for list item labels.

```python
doc = aw.Document()

list = doc.lists.add(aw.lists.ListTemplate.BULLET_CIRCLE)

# Create a picture bullet for the current list level, and set an image from a local file system
# as the icon that the bullets for this list level will display.
list.list_levels[0].create_picture_bullet()
list.list_levels[0].image_data.set_image(IMAGE_DIR + "Logo icon.ico")

self.assertTrue(list.list_levels[0].image_data.has_image)

builder = aw.DocumentBuilder(doc)

builder.list_format.list = list
builder.writeln("Hello world!")
builder.write("Hello again!")

doc.save(ARTIFACTS_DIR + "Lists.create_picture_bullet.docx")

list.list_levels[0].delete_picture_bullet()

self.assertIsNone(list.list_levels[0].image_data)
```

### See Also

* module [aspose.words.lists](../../)
* class [ListLevel](../)

