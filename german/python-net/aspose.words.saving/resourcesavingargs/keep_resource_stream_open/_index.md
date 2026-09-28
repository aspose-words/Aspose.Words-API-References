---
title: ResourceSavingArgs.keep_resource_stream_open property
linktitle: keep_resource_stream_open property
articleTitle: keep_resource_stream_open property
second_title: Aspose.Words for Python
description: "ResourceSavingArgs.keep_resource_stream_open property. Specifies whether Aspose.Words should keep the stream open or close it after saving a resource."
type: docs
weight: 20
url: /de/python-net/aspose.words.saving/resourcesavingargs/keep_resource_stream_open/
---

## ResourceSavingArgs.keep_resource_stream_open property

Specifies whether Aspose.Words should keep the stream open or close it after saving a resource.


```python
@property
def keep_resource_stream_open(self) -> bool:
    ...

@keep_resource_stream_open.setter
def keep_resource_stream_open(self, value: bool):
    ...

```

### Remarks

Default is ``False`` and Aspose.Words will close the stream you provided
in the [ResourceSavingArgs.resource_stream](../resource_stream/) property after writing a resource into it.
Specify ``True`` to keep the stream open.




### Examples

Shows how to use a callback to print the URIs of external resources created while converting a document to HTML (ResourceUriPrinter).

```python
class ResourceUriPrinter(aw.saving.IResourceSavingCallback):

    def __init__(self):
        self.m_saved_resource_count = None
        self.m_text = []

    def resource_saving(self, args):
        # Wenn wir einen Ordneralias im SaveOptions-Objekt festlegen, können wir ihn hier ausdrucken.
        self.m_saved_resource_count += 1
        self.m_text.append(f'Resource #{self.m_saved_resource_count} "{args.resource_file_name}"')
        extension = Path(args.resource_file_name).suffix
        if extension in ('.ttf', '.woff'):
            # Standardmäßig verwendet 'ResourceFileUri' den Systemordner für Schriftarten.
            # Um Probleme auf anderen Plattformen zu vermeiden, müssen Sie den Pfad für die Schriftarten explizit angeben.
            args.resource_file_uri = str(Path(ARTIFACTS_DIR) / args.resource_file_name)
        self.m_text.append('\t' + args.resource_file_uri + '\n')
        # Wenn wir einen Ordner in der "ResourcesFolderAlias"-Eigenschaft angegeben haben,
        # müssen wir außerdem jeden Stream umleiten, damit seine Ressource in diesem Ordner abgelegt wird.
        args.resource_stream = system_helper.io.FileStream(args.resource_file_uri, system_helper.io.FileMode.CREATE)
        args.keep_resource_stream_open = False

    def get_text(self):
        return str.join('', self.m_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [ResourceSavingArgs](../)
* property [ResourceSavingArgs.resource_stream](../resource_stream/)

