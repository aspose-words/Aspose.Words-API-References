---
title: HtmlFixedSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "HtmlFixedSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 190
url: /es/python-net/aspose.words.saving/htmlfixedsaveoptions/save_format/
---

## HtmlFixedSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.HTML_FIXED](../../../aspose.words/saveformat/#HTML_FIXED).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
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
        # Si establecemos un alias de carpeta en el objeto SaveOptions, podremos imprimirlo desde aquí.
        self.m_saved_resource_count += 1
        self.m_text.append(f'Resource #{self.m_saved_resource_count} "{args.resource_file_name}"')
        extension = Path(args.resource_file_name).suffix
        if extension in ('.ttf', '.woff'):
            # Por defecto, 'ResourceFileUri' usa la carpeta del sistema para fuentes.
            # Para evitar problemas en otras plataformas debe especificar explícitamente la ruta de las fuentes.
            args.resource_file_uri = str(Path(ARTIFACTS_DIR) / args.resource_file_name)
        self.m_text.append('\t' + args.resource_file_uri + '\n')
        # Si hemos especificado una carpeta en la propiedad "ResourcesFolderAlias",
        # también necesitaremos redirigir cada flujo para colocar su recurso en esa carpeta.
        args.resource_stream = system_helper.io.FileStream(args.resource_file_uri, system_helper.io.FileMode.CREATE)
        args.keep_resource_stream_open = False

    def get_text(self):
        return str.join('', self.m_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

