---
title: DocumentBase.resource_loading_callback property
linktitle: resource_loading_callback property
articleTitle: resource_loading_callback property
second_title: Aspose.Words for Python
description: "DocumentBase.resource_loading_callback property. Allows to control how external resources are loaded."
type: docs
weight: 80
url: /python-net/aspose.words/documentbase/resource_loading_callback/
---

## DocumentBase.resource_loading_callback property

Allows to control how external resources are loaded.


```python
@property
def resource_loading_callback(self) -> aspose.words.loading.IResourceLoadingCallback:
    ...

@resource_loading_callback.setter
def resource_loading_callback(self, value: aspose.words.loading.IResourceLoadingCallback):
    ...

```

### Examples

Shows how to customize the process of loading external resources into a document (ImageNameHandler).

```python
class ImageNameHandler(aw.loading.IResourceLoadingCallback):

    def resource_loading(self, args):
        # If this callback encounters one of the image shorthands while loading an image,
        # it will apply unique logic for each defined shorthand instead of treating it as a URI.
        if args.resource_type == aw.loading.ResourceType.IMAGE:
            switch_condition = args.original_uri
            if switch_condition == 'Google logo':
                import requests
                image_data = requests.get('http://www.google.com/images/logos/ps_logo2.png').content
                args.set_data(image_data)
                return aw.loading.ResourceLoadingAction.USER_PROVIDED
            elif switch_condition == 'Aspose logo':
                from api_example_base import IMAGE_DIR
                args.set_data(open(IMAGE_DIR + 'Logo.jpg', 'rb').read())
                return aw.loading.ResourceLoadingAction.USER_PROVIDED
            elif switch_condition == 'Watermark':
                args.set_data(open(IMAGE_DIR + 'Transparent background logo.png', 'rb').read())
                return aw.loading.ResourceLoadingAction.USER_PROVIDED
        return aw.loading.ResourceLoadingAction.DEFAULT
```

### See Also

* module [aspose.words](../../)
* class [DocumentBase](../)

