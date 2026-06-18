---
title: ResourceLoadingArgs class
linktitle: ResourceLoadingArgs class
articleTitle: ResourceLoadingArgs class
second_title: Aspose.Words for Python
description: "aspose.words.loading.ResourceLoadingArgs class. Provides data for the [IResourceLoadingCallback.resource_loading()](../iresourceloadingcallback/resource_loading/#resourceloadingargs) method."
type: docs
weight: 160
url: /python-net/aspose.words.loading/resourceloadingargs/
---

## ResourceLoadingArgs class

Provides data for the [IResourceLoadingCallback.resource_loading()](../iresourceloadingcallback/resource_loading/#resourceloadingargs) method.



### Properties

| Name | Description |
| --- | --- |
| [original_uri](./original_uri/) | Original URI of the resource as specified in imported document. |
| [resource_type](./resource_type/) | Type of resource. |
| [uri](./uri/) | URI of the resource which is used for downloading if [IResourceLoadingCallback.resource_loading()](../iresourceloadingcallback/resource_loading/#resourceloadingargs) returns [ResourceLoadingAction.DEFAULT](../resourceloadingaction/#DEFAULT). |

### Methods

| Name | Description |
| --- | --- |
|[ set_data(data)](./set_data/#bytes) | Sets user provided data of the resource which is used if [IResourceLoadingCallback.resource_loading()](../iresourceloadingcallback/resource_loading/#resourceloadingargs) returns [ResourceLoadingAction.USER_PROVIDED](../resourceloadingaction/#USER_PROVIDED). |

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

* module [aspose.words.loading](../)

