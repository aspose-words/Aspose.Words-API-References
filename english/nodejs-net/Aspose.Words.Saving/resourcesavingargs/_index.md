---
title: ResourceSavingArgs class
linktitle: ResourceSavingArgs class
articleTitle: ResourceSavingArgs class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.ResourceSavingArgs class. Provides data for the [IResourceSavingCallback.resourceSaving()](../iresourcesavingcallback/resourceSaving/#resourcesavingargs) event"
type: docs
weight: 760
url: /nodejs-net/aspose.words.saving/resourcesavingargs/
---

## ResourceSavingArgs class

Provides data for the [IResourceSavingCallback.resourceSaving()](../iresourcesavingcallback/resourceSaving/#resourcesavingargs) event.
To learn more, visit the [Save a Document](https://docs.aspose.com/words/nodejs-net/save-a-document/) documentation article.




### Remarks

By default, when Aspose.Words saves a document to fixed page HTML or SVG, it saves each resource into 
a separate file. Aspose.Words uses the document file name and a unique number to generate unique file name
for each resource found in the document.

[ResourceSavingArgs](./) allows to redefine how resource file names are generated or to 
completely circumvent saving of resources into files by providing your own stream objects.

To apply your own logic for generating resource file names use the 
[ResourceSavingArgs.resourceFileName](./resourceFileName/) property.

To save resources into streams instead of files, use the Aspose.Words.Saving.ResourceSavingArgs.ResourceStream property.




### Properties

| Name | Description |
| --- | --- |
| [document](./document/) | Gets the document object that is currently being saved. |
| [keepResourceStreamOpen](./keepResourceStreamOpen/) | Specifies whether Aspose.Words should keep the stream open or close it after saving a resource. |
| [resourceFileName](./resourceFileName/) | Gets or sets the file name (without path) where the resource will be saved to. |
| [resourceFileUri](./resourceFileUri/) | Gets or sets the uniform resource identifier (URI) used to reference the resource file from the document. |

### See Also

* module [Aspose.Words.Saving](../)

