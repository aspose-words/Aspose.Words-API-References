---
title: HtmlFixedSaveOptions.resource_saving_callback property
linktitle: resource_saving_callback property
articleTitle: resource_saving_callback property
second_title: Aspose.Words for Python
description: "HtmlFixedSaveOptions.resource_saving_callback property. Allows to control how resources (images, fonts and css) are saved when a document is exported to fixed page Html format."
type: docs
weight: 150
url: /it/python-net/aspose.words.saving/htmlfixedsaveoptions/resource_saving_callback/
---

## HtmlFixedSaveOptions.resource_saving_callback property

Allows to control how resources (images, fonts and css) are saved when a document is exported to fixed page Html format.


```python
@property
def resource_saving_callback(self) -> aspose.words.saving.IResourceSavingCallback:
    ...

@resource_saving_callback.setter
def resource_saving_callback(self, value: aspose.words.saving.IResourceSavingCallback):
    ...

```

### Examples

Shows how to use a callback to print the URIs of external resources created while converting a document to HTML (ResourceUriPrinter).

```python
class ResourceUriPrinter(aw.saving.IResourceSavingCallback):

    def __init__(self):
        self.m_saved_resource_count = None
        self.m_text = []

    def resource_saving(self, args):
        # Se impostiamo un alias di cartella nell'oggetto SaveOptions, potremo stamparlo da qui.
        self.m_saved_resource_count += 1
        self.m_text.append(f'Resource #{self.m_saved_resource_count} "{args.resource_file_name}"')
        extension = Path(args.resource_file_name).suffix
        if extension in ('.ttf', '.woff'):
            # Per impostazione predefinita, 'ResourceFileUri' utilizza la cartella di sistema per i font.
            # Per evitare problemi su altre piattaforme devi specificare esplicitamente il percorso per i font.
            args.resource_file_uri = str(Path(ARTIFACTS_DIR) / args.resource_file_name)
        self.m_text.append('\t' + args.resource_file_uri + '\n')
        # Se abbiamo specificato una cartella nella proprietà "ResourcesFolderAlias",
        # dovremo anche reindirizzare ogni stream per inserire la sua risorsa in quella cartella.
        args.resource_stream = system_helper.io.FileStream(args.resource_file_uri, system_helper.io.FileMode.CREATE)
        args.keep_resource_stream_open = False

    def get_text(self):
        return str.join('', self.m_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

