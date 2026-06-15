---
title: ResourceLoadingAction enumeration
linktitle: ResourceLoadingAction enumeration
articleTitle: ResourceLoadingAction enumeration
second_title: Aspose.Words for Python
description: "aspose.words.loading.ResourceLoadingAction enumeration. Specifies the mode of resource loading"
type: docs
weight: 150
url: /python-net/aspose.words.loading/resourceloadingaction/
---

## ResourceLoadingAction enumeration

Specifies the mode of resource loading.
To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/python-net/specify-load-options/) documentation article.




### Members

| Name | Description |
| --- | --- |
| DEFAULT | Aspose.Words will load this resource as usual. |
| SKIP | Aspose.Words will skip loading of this resource. Only link without data will be stored for an image, CSS style sheet will be ignored for HTML format. |
| USER_PROVIDED | Aspose.Words will use byte array provided by user in [ResourceLoadingArgs.set_data()](../resourceloadingargs/set_data/#bytes) as resource data. |

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

