---
title: License constructor
linktitle: License constructor
articleTitle: License constructor
second_title: Aspose.Words for Python
description: "License constructor. Initializes a new instance of this class."
type: docs
weight: 10
url: /ru/python-net/aspose.words/license/__init__/
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
# Установите лицензию для нашего продукта Aspose.Words, передав имя файла действующей лицензии в локальной файловой системе.
license_file_name = os.path.join(LICENSE_PATH, test_license_file_name)
license = aw.License()
license.set_license(license_name=license_file_name)
# Создайте копию нашего лицензионного файла в папке binaries вашего приложения.
license_copy_file_name = os.path.join(AssemblyDir, test_license_file_name)
shutil.copy2(license_file_name, license_copy_file_name)
# Если мы передадим имя файла без пути,
# Метод SetLicense будет искать этот файл в нескольких локальных местах файловой системы.
# Одним из этих мест будет папка "bin", которая содержит копию нашего файла лицензии.
license.set_license(license_name=test_license_file_name)
```

### See Also

* module [aspose.words](../../)
* class [License](../)

