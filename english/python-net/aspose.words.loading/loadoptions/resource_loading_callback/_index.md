---
title: LoadOptions.resource_loading_callback property
linktitle: resource_loading_callback property
articleTitle: resource_loading_callback property
second_title: Aspose.Words for Python
description: "LoadOptions.resource_loading_callback property. Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML."
type: docs
weight: 150
url: /python-net/aspose.words.loading/loadoptions/resource_loading_callback/
---

## LoadOptions.resource_loading_callback property

Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML.


```python
@property
def resource_loading_callback(self) -> aspose.words.loading.IResourceLoadingCallback:
    ...

@resource_loading_callback.setter
def resource_loading_callback(self, value: aspose.words.loading.IResourceLoadingCallback):
    ...

```

### Examples

Shows how to handle external resources when loading Html documents (HtmlLinkedResourceLoadingCallback).

```python
class HtmlLinkedResourceLoadingCallback(aw.loading.IResourceLoadingCallback):

    def resource_loading(self, args):
        switch_condition = args.resource_type
        if switch_condition == aw.loading.ResourceType.CSS_STYLE_SHEET:
            print(f'External CSS Stylesheet found upon loading: {args.original_uri}')
            return aw.loading.ResourceLoadingAction.DEFAULT
        elif switch_condition == aw.loading.ResourceType.IMAGE:
            print(f'External Image found upon loading: {args.original_uri}')
            new_image_filename = 'Logo.jpg'
            print(f'\tImage will be substituted with: {new_image_filename}')
            new_image = Image.from_file(IMAGE_DIR + new_image_filename)
            converter = ImageConverter()
            image_bytes = converter.convert_to(new_image, bytes)
            args.set_data(image_bytes)
            return aw.loading.ResourceLoadingAction.USER_PROVIDED
        return aw.loading.ResourceLoadingAction.DEFAULT
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

