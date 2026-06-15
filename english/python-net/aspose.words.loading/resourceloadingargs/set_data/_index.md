---
title: ResourceLoadingArgs.set_data method
linktitle: set_data method
articleTitle: set_data method
second_title: Aspose.Words for Python
description: "ResourceLoadingArgs.set_data method. Sets user provided data of the resource which is used if [IResourceLoadingCallback.resource_loading()](../../iresourceloadingcallback/resource_loading/#resourceloadingargs) returns [ResourceLoadingAction.USER_PROVIDED](../../resourceloadingaction/#USER_PROVIDED)."
type: docs
weight: 40
url: /python-net/aspose.words.loading/resourceloadingargs/set_data/
---

## set_data(data) {#bytes}

Sets user provided data of the resource which is used
if [IResourceLoadingCallback.resource_loading()](../../iresourceloadingcallback/resource_loading/#resourceloadingargs)
returns [ResourceLoadingAction.USER_PROVIDED](../../resourceloadingaction/#USER_PROVIDED).



```python
def set_data(self, data: bytes):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| data | bytes |  |

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

* module [aspose.words.loading](../../)
* class [ResourceLoadingArgs](../)

