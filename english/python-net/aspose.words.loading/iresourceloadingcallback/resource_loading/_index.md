---
title: IResourceLoadingCallback.resource_loading method
linktitle: resource_loading method
articleTitle: resource_loading method
second_title: Aspose.Words for Python
description: "IResourceLoadingCallback.resource_loading method. Called when Aspose.Words loads any external resource."
type: docs
weight: 10
url: /python-net/aspose.words.loading/iresourceloadingcallback/resource_loading/
---

## resource_loading(args) {#resourceloadingargs}

Called when Aspose.Words loads any external resource.


```python
def resource_loading(self, args: aspose.words.loading.ResourceLoadingArgs):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| args | [ResourceLoadingArgs](../../resourceloadingargs/) |  |

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
* class [IResourceLoadingCallback](../)

