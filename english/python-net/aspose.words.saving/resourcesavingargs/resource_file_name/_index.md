---
title: ResourceSavingArgs.resource_file_name property
linktitle: resource_file_name property
articleTitle: resource_file_name property
second_title: Aspose.Words for Python
description: "ResourceSavingArgs.resource_file_name property. Gets or sets the file name (without path) where the resource will be saved to."
type: docs
weight: 30
url: /python-net/aspose.words.saving/resourcesavingargs/resource_file_name/
---

## ResourceSavingArgs.resource_file_name property

Gets or sets the file name (without path) where the resource will be saved to.


```python
@property
def resource_file_name(self) -> str:
    ...

@resource_file_name.setter
def resource_file_name(self, value: str):
    ...

```

### Remarks

This property allows you to redefine how the resource file names are generated
during export to fixed page HTML or SVG.

When the event is fired, this property contains the file name that was generated 
by Aspose.Words. You can change the value of this property to save the resource into a 
different file. Note that file names must be unique.

Aspose.Words automatically generates a unique file name for every resource when 
exporting to fixed page HTML or SVG format. How the resource file name is generated 
depends on whether you save the document to a file or to a stream.

When saving a document to a file, the generated resource file name looks like 
*\<document base file name\>.\<image number\>.\<extension\>*.

When saving a document to a stream, the generated resource file name looks like 
*Aspose.Words.\<document guid\>.\<image number\>.\<extension\>*.

[ResourceSavingArgs.resource_file_name](./) must contain only the file name without the path.
Aspose.Words determines the path for saving and the value of the ``src`` attribute for writing 
to fixed page HTML or SVG using the document file name, the [HtmlFixedSaveOptions.resources_folder](../../htmlfixedsaveoptions/resources_folder/)
or [SvgSaveOptions.resources_folder](../../svgsaveoptions/resources_folder/) and [HtmlFixedSaveOptions.resources_folder_alias](../../htmlfixedsaveoptions/resources_folder_alias/) 
or [SvgSaveOptions.resources_folder_alias](../../svgsaveoptions/resources_folder_alias/) properties.

[HtmlFixedSaveOptions.resources_folder](../../htmlfixedsaveoptions/resources_folder/)
[SvgSaveOptions.resources_folder](../../svgsaveoptions/resources_folder/)
[HtmlFixedSaveOptions.resources_folder_alias](../../htmlfixedsaveoptions/resources_folder_alias/)
[SvgSaveOptions.resources_folder_alias](../../svgsaveoptions/resources_folder_alias/)



### See Also

* module [aspose.words.saving](../../)
* class [ResourceSavingArgs](../)
* property [ResourceSavingArgs.resource_stream](../resource_stream/)

