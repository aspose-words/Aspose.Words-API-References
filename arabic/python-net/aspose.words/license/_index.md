---
title: License class
linktitle: License class
articleTitle: License class
second_title: Aspose.Words for Python
description: "aspose.words.License class. Provides methods to license the component"
type: docs
weight: 710
url: /ar/python-net/aspose.words/license/
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

* module [aspose.words](../)

