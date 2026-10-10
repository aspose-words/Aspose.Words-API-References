---
title: License constructor
linktitle: License constructor
articleTitle: License constructor
second_title: Aspose.Words for Python
description: "License constructor. Initializes a new instance of this class."
type: docs
weight: 10
url: /ar/python-net/aspose.words/license/__init__/
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
# حدد الترخيص لمنتج Aspose.Words الخاص بنا بتمرير اسم ملف الترخيص الصالح من نظام الملفات المحلي.
license_file_name = os.path.join(LICENSE_PATH, test_license_file_name)
license = aw.License()
license.set_license(license_name=license_file_name)
# أنشئ نسخة من ملف الترخيص في مجلد الثنائيات لتطبيقنا.
license_copy_file_name = os.path.join(AssemblyDir, test_license_file_name)
shutil.copy2(license_file_name, license_copy_file_name)
# إذا مررنا اسم ملف دون مسار،
# ستقوم SetLicense بالبحث في عدة مواقع على نظام الملفات المحلي عن هذا الملف.
# إحدى تلك المواقع ستكون مجلد \"bin\"، الذي يحتوي على نسخة من ملف الترخيص الخاص بنا.
license.set_license(license_name=test_license_file_name)
```

### See Also

* module [aspose.words](../../)
* class [License](../)

