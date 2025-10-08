---
title: ResourceSavingArgs.resource_file_uri property
linktitle: resource_file_uri property
articleTitle: resource_file_uri property
second_title: Aspose.Words for Python
description: "ResourceSavingArgs.resource_file_uri property. Gets or sets the uniform resource identifier (URI) used to reference the resource file from the document."
type: docs
weight: 40
url: /python-net/aspose.words.saving/resourcesavingargs/resource_file_uri/
---

## ResourceSavingArgs.resource_file_uri property

Gets or sets the uniform resource identifier (URI) used to reference the resource file from the document.


```python
@property
def resource_file_uri(self) -> str:
    ...

@resource_file_uri.setter
def resource_file_uri(self, value: str):
    ...

```

### Remarks

This property allows you to change URIs of resource files exported to fixed page HTML,
SVG or Markdown documents.

Aspose.Words automatically generates an URI for every resource file during export to fixed page HTML,
SVG or Markdown format. The generated URIs reference resource files saved by Aspose.Words. However, the URIs
can be incorrect if resource files are to be moved to other location or if resource files are saved to streams.
This property allows to correct URIs in these cases.

When the event is fired, this property contains the URI that was generated
by Aspose.Words. You can change the value of this property to provide a custom URI for the resource file.

[HtmlFixedSaveOptions.resources_folder](../../htmlfixedsaveoptions/resources_folder/)
[SvgSaveOptions.resources_folder](../../svgsaveoptions/resources_folder/)
[MarkdownSaveOptions.images_folder](../../markdownsaveoptions/images_folder/)
[HtmlFixedSaveOptions.resources_folder_alias](../../htmlfixedsaveoptions/resources_folder_alias/)
[SvgSaveOptions.resources_folder_alias](../../svgsaveoptions/resources_folder_alias/)
[MarkdownSaveOptions.images_folder_alias](../../markdownsaveoptions/images_folder_alias/)



### See Also

* module [aspose.words.saving](../../)
* class [ResourceSavingArgs](../)

