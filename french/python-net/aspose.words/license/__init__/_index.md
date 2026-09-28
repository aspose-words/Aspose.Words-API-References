---
title: License constructor
linktitle: License constructor
articleTitle: License constructor
second_title: Aspose.Words for Python
description: "License constructor. Initializes a new instance of this class."
type: docs
weight: 10
url: /fr/python-net/aspose.words/license/__init__/
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
# Définissez la licence de notre produit Aspose.Words en passant le nom de fichier du système de fichiers local d'un fichier de licence valide.
license_file_name = os.path.join(LICENSE_PATH, test_license_file_name)
license = aw.License()
license.set_license(license_name=license_file_name)
# Créez une copie de notre fichier de licence dans le dossier binaries de notre application.
license_copy_file_name = os.path.join(AssemblyDir, test_license_file_name)
shutil.copy2(license_file_name, license_copy_file_name)
# Si nous transmettons le nom d'un fichier sans chemin,
# la SetLicense recherchera plusieurs emplacements du système de fichiers local pour ce fichier.
# L'un de ces emplacements sera le dossier "bin", qui contient une copie de notre fichier de licence.
license.set_license(license_name=test_license_file_name)
```

### See Also

* module [aspose.words](../../)
* class [License](../)

