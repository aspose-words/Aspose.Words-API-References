---
title: License class
linktitle: License class
articleTitle: License class
second_title: Aspose.Words for Python
description: "aspose.words.License class. Provides methods to license the component"
type: docs
weight: 710
url: /sv/python-net/aspose.words/license/
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

### See Also

* module [aspose.words](../)

