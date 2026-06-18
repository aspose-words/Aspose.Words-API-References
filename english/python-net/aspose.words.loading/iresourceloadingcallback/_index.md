---
title: IResourceLoadingCallback class
linktitle: IResourceLoadingCallback class
articleTitle: IResourceLoadingCallback class
second_title: Aspose.Words for Python
description: "aspose.words.loading.IResourceLoadingCallback class. Implement this interface if you want to control how Aspose.Words loads external resource when  importing a document and inserting images using [DocumentBuilder](../../aspose.words/documentbuilder/)."
type: docs
weight: 100
url: /python-net/aspose.words.loading/iresourceloadingcallback/
---

## IResourceLoadingCallback class

Implement this interface if you want to control how Aspose.Words loads external resource when 
importing a document and inserting images using [DocumentBuilder](../../aspose.words/documentbuilder/).



### Methods

| Name | Description |
| --- | --- |
|[ resource_loading(args)](./resource_loading/#resourceloadingargs) | Called when Aspose.Words loads any external resource. |

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

