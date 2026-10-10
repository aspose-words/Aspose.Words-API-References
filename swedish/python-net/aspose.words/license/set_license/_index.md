---
title: License.set_license method
linktitle: set_license method
articleTitle: set_license method
second_title: Aspose.Words for Python
description: "aspose.words.License.set_license method"
type: docs
weight: 20
url: /sv/python-net/aspose.words/license/set_license/
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
# Ställ in licensen för vår Aspose.Words-produkt genom att skicka filnamnet på en giltig licensfil i det lokala filsystemet.
license_file_name = os.path.join(LICENSE_PATH, test_license_file_name)
license = aw.License()
license.set_license(license_name=license_file_name)
# Skapa en kopia av vår licensfil i binärkatalogen för vår applikation.
license_copy_file_name = os.path.join(AssemblyDir, test_license_file_name)
shutil.copy2(license_file_name, license_copy_file_name)
# Om vi skickar ett fils namn utan en sökväg,
# SetLicense kommer att söka igenom flera lokala filsystemplatser efter den här filen.
# En av dessa platser kommer att vara "bin"-mappen, som innehåller en kopia av vår licensfil.
license.set_license(license_name=test_license_file_name)
```

Shows how to initialize a license for Aspose.Words from a stream.

```python
# Ställ in licensen för vår Aspose.Words-produkt genom att skicka en ström för en giltig licensfil i vårt lokala filsystem.
with system_helper.io.File.open_read(LICENSE_PATH) as my_stream:
    license = aw.License()
    license.set_license(stream=my_stream)
```

## See Also

* module [aspose.words](../../)
* class [License](../)

