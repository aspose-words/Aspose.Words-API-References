---
title: License constructor
linktitle: License constructor
articleTitle: License constructor
second_title: Aspose.Words for Python
description: "License constructor. Initializes a new instance of this class."
type: docs
weight: 10
url: /de/python-net/aspose.words/license/__init__/
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
# Setze die Lizenz für unser Aspose.Words-Produkt, indem du den Dateinamen einer gültigen Lizenzdatei aus dem lokalen Dateisystem übergibst.
license_file_name = os.path.join(LICENSE_PATH, test_license_file_name)
license = aw.License()
license.set_license(license_name=license_file_name)
# Erstelle eine Kopie unserer Lizenzdatei im Binärordner unserer Anwendung.
license_copy_file_name = os.path.join(AssemblyDir, test_license_file_name)
shutil.copy2(license_file_name, license_copy_file_name)
# Wenn wir einen Dateinamen ohne Pfad übergeben,
# Die SetLicense wird an mehreren lokalen Dateisystem‑Standorten nach dieser Datei suchen.
# Einer dieser Orte wird der "bin"‑Ordner sein, der eine Kopie unserer Lizenzdatei enthält.
license.set_license(license_name=test_license_file_name)
```

### See Also

* module [aspose.words](../../)
* class [License](../)

