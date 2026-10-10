---
title: License.set_license method
linktitle: set_license method
articleTitle: set_license method
second_title: Aspose.Words for Python
description: "aspose.words.License.set_license method"
type: docs
weight: 20
url: /es/python-net/aspose.words/license/set_license/
---

## set_license(license_name) {#str}

Licenses the component.


```python
def set_license(self, license_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| license_name | str | Can be a full or short file name or name of an embedded resource. Use an empty string to switch to evaluation mode. |

### Remarks

Tries to find the license in the following locations:

1. Explicit path.

2. The folder that contains the Aspose component assembly.

3. The folder that contains the client's calling assembly.

4. The folder that contains the entry (startup) assembly.

5. An embedded resource in the client's calling assembly.

**Note:** On the .NET Compact Framework, tries to find the license only in these locations:

1. Explicit path.

2. An embedded resource in the client's calling assembly.




## set_license(stream) {#bytesio}

Licenses the component.


```python
def set_license(self, stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO | A stream that contains the license. |

### Remarks

Use this method to load a license from a stream.




## Examples

Shows how to initialize a license for Aspose.Words using a license file in the local file system.

```python
import os
import shutil
test_license_file_name = 'Aspose.Total.NET.lic'
# Establecer la licencia para nuestro producto Aspose.Words pasando el nombre de archivo del sistema de archivos local de un archivo de licencia válido.
license_file_name = os.path.join(LICENSE_PATH, test_license_file_name)
license = aw.License()
license.set_license(license_name=license_file_name)
# Crear una copia de nuestro archivo de licencia en la carpeta binaria de nuestra aplicación.
license_copy_file_name = os.path.join(AssemblyDir, test_license_file_name)
shutil.copy2(license_file_name, license_copy_file_name)
# Si pasamos el nombre de un archivo sin una ruta,
# el SetLicense buscará varias ubicaciones del sistema de archivos local para este archivo.
# Una de esas ubicaciones será la carpeta "bin", que contiene una copia de nuestro archivo de licencia.
license.set_license(license_name=test_license_file_name)
```

Shows how to initialize a license for Aspose.Words from a stream.

```python
# Establezca la licencia para nuestro producto Aspose.Words pasando un flujo para un archivo de licencia válido en nuestro sistema de archivos local.
with system_helper.io.File.open_read(LICENSE_PATH) as my_stream:
    license = aw.License()
    license.set_license(stream=my_stream)
```

## See Also

* module [aspose.words](../../)
* class [License](../)

