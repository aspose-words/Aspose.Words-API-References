---
title: License class
linktitle: License class
articleTitle: License class
second_title: Aspose.Words for Python
description: "aspose.words.License class. Provides methods to license the component"
type: docs
weight: 710
url: /tr/python-net/aspose.words/license/
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
# Aspose.Words ürünümüz için lisansı, geçerli bir lisans dosyasının yerel dosya sistemi dosya adını geçirerek ayarlayın.
license_file_name = os.path.join(LICENSE_PATH, test_license_file_name)
license = aw.License()
license.set_license(license_name=license_file_name)
# Uygulamamızın binaries klasöründe lisans dosyamızın bir kopyasını oluşturun.
license_copy_file_name = os.path.join(AssemblyDir, test_license_file_name)
shutil.copy2(license_file_name, license_copy_file_name)
# Eğer bir dosyanın adını yol olmadan geçirirsek,
# SetLicense, bu dosya için birkaç yerel dosya sistemi konumunu arayacaktır.
# Bu konumlardan biri "bin" klasörü olacaktır, bu klasör lisans dosyamızın bir kopyasını içerir.
license.set_license(license_name=test_license_file_name)
```

### See Also

* module [aspose.words](../)

