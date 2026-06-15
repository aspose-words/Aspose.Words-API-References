---
title: ResourceType enumeration
linktitle: ResourceType enumeration
articleTitle: ResourceType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.loading.ResourceType enumeration. Type of loaded resource."
type: docs
weight: 170
url: /python-net/aspose.words.loading/resourcetype/
---

## ResourceType enumeration

Type of loaded resource.


### Members

| Name | Description |
| --- | --- |
| IMAGE | Image. |
| FONT | Font. |
| CSS_STYLE_SHEET | CSS style sheet. |
| DOCUMENT | Document. |

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

