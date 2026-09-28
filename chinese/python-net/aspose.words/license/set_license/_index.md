---
title: License.set_license method
linktitle: set_license method
articleTitle: set_license method
second_title: Aspose.Words for Python
description: "aspose.words.License.set_license method"
type: docs
weight: 20
url: /zh/python-net/aspose.words/license/set_license/
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
# 通过传递有效许可证文件的本地文件系统文件名，为我们的 Aspose.Words 产品设置许可证。
license_file_name = os.path.join(LICENSE_PATH, test_license_file_name)
license = aw.License()
license.set_license(license_name=license_file_name)
# 在应用程序的 binaries 文件夹中创建许可证文件的副本。
license_copy_file_name = os.path.join(AssemblyDir, test_license_file_name)
shutil.copy2(license_file_name, license_copy_file_name)
# 如果我们传递没有路径的文件名，
# SetLicense 将在多个本地文件系统位置搜索此文件。
# 其中一个位置将是 "bin" 文件夹，其中包含我们的许可证文件的副本。
license.set_license(license_name=test_license_file_name)
```

Shows how to initialize a license for Aspose.Words from a stream.

```python
# 通过传入本地文件系统中有效许可证文件的流，为我们的 Aspose.Words 产品设置许可证。
with system_helper.io.File.open_read(LICENSE_PATH) as my_stream:
    license = aw.License()
    license.set_license(stream=my_stream)
```

## See Also

* module [aspose.words](../../)
* class [License](../)

