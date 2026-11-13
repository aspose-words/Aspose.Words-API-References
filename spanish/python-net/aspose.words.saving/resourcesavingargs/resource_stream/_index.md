---
title: ResourceSavingArgs.resource_stream property
linktitle: resource_stream property
articleTitle: resource_stream property
second_title: Aspose.Words for Python
description: "ResourceSavingArgs.resource_stream property. Allows to specify the stream where the resource will be saved to."
type: docs
weight: 50
url: /es/python-net/aspose.words.saving/resourcesavingargs/resource_stream/
---

## ResourceSavingArgs.resource_stream property

Allows to specify the stream where the resource will be saved to.


```python
@property
def resource_stream(self) -> io.BytesIO:
    ...

@resource_stream.setter
def resource_stream(self, value: io.BytesIO):
    ...

```

### Remarks

This property allows you to save resources to streams instead of files.

The default value is ``None``. When this property is ``None``, the resource
will be saved to a file specified in the [ResourceSavingArgs.resource_file_name](../resource_file_name/) property.

Using [IResourceSavingCallback](../../iresourcesavingcallback/) you cannot substitute one resource with
another. It is intended only for control over location where to save resources.




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
* class [ResourceSavingArgs](../)
* property [ResourceSavingArgs.resource_file_name](../resource_file_name/)
* property [ResourceSavingArgs.keep_resource_stream_open](../keep_resource_stream_open/)

