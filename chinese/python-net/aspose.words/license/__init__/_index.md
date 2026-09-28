---
title: License constructor
linktitle: License constructor
articleTitle: License constructor
second_title: Aspose.Words for Python
description: "License constructor. Initializes a new instance of this class."
type: docs
weight: 10
url: /zh/python-net/aspose.words/license/__init__/
---

## License() {#default}

Initializes a new instance of this class.


```python
def __init__(self):
    ...
```

### Examples

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

### See Also

* module [aspose.words](../../)
* class [License](../)

