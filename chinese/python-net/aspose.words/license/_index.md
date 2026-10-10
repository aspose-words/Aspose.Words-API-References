---
title: License class
linktitle: License class
articleTitle: License class
second_title: Aspose.Words for Python
description: "aspose.words.License class. Provides methods to license the component"
type: docs
weight: 710
url: /zh/python-net/aspose.words/license/
---

## License class

Provides methods to license the component.
To learn more, visit the [Licensing and Subscription](https://docs.aspose.com/words/python-net/licensing/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [License()](./__init__/#default) | Initializes a new instance of this class. |

### Methods

| Name | Description |
| --- | --- |
|[ set_license(license_name)](./set_license/#str) | Licenses the component. |
|[ set_license(stream)](./set_license/#bytesio) | Licenses the component. |

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

* module [aspose.words](../)

