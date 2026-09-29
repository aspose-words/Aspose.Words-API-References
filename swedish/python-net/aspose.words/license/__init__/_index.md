---
title: License constructor
linktitle: License constructor
articleTitle: License constructor
second_title: Aspose.Words for Python
description: "License constructor. Initializes a new instance of this class."
type: docs
weight: 10
url: /sv/python-net/aspose.words/license/__init__/
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

* module [aspose.words](../../)
* class [License](../)

