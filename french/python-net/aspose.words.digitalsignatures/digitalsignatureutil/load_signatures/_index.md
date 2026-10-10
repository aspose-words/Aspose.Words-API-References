---
title: DigitalSignatureUtil.load_signatures method
linktitle: load_signatures method
articleTitle: load_signatures method
second_title: Aspose.Words for Python
description: "aspose.words.digitalsignatures.DigitalSignatureUtil.load_signatures method"
type: docs
weight: 10
url: /fr/python-net/aspose.words.digitalsignatures/digitalsignatureutil/load_signatures/
---

## load_signatures(file_name) {#str}

Loads digital signatures from document.


```python
def load_signatures(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | Path to the document. |

### Returns

Collection of digital signatures. Returns empty collection if file is not signed.


## load_signatures(stream) {#bytesio}

Loads digital signatures from document using stream.


```python
def load_signatures(self, stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO | Stream with the document. |

### Returns

Collection of digital signatures. Returns empty collection if file is not signed.


## Examples

Shows how to load signatures from a digitally signed document.

```python
# Il existe deux manières de charger la collection de signatures numériques d'un document signé en utilisant la classe DigitalSignatureUtil.
# 1 -  Charger à partir d'un document depuis un nom de fichier du système de fichiers local:
digital_signatures = aw.digitalsignatures.DigitalSignatureUtil.load_signatures(file_name=MY_DIR + 'Digitally signed.docx')
# Si cette collection n'est pas vide, alors nous pouvons vérifier que le document est signé numériquement.
self.assertEqual(1, digital_signatures.count)
# 2 -  Charger à partir d'un document depuis un FileStream:
with system_helper.io.FileStream(MY_DIR + 'Digitally signed.docx', system_helper.io.FileMode.OPEN) as stream:
    digital_signatures = aw.digitalsignatures.DigitalSignatureUtil.load_signatures(stream=stream)
    self.assertEqual(1, digital_signatures.count)
```

Shows how to remove digital signatures from a digitally signed document.

```python
# Il existe deux façons d'utiliser la classe DigitalSignatureUtil pour supprimer les signatures numériques
# à partir d'un document signé en enregistrant une copie non signée ailleurs dans le système de fichiers local.
# 1 - Déterminer les emplacements du document signé et de la copie non signée à l'aide de chaînes de noms de fichiers:
aw.digitalsignatures.DigitalSignatureUtil.remove_all_signatures(src_file_name=MY_DIR + 'Digitally signed.docx', dst_file_name=ARTIFACTS_DIR + 'DigitalSignatureUtil.LoadAndRemove.FromString.docx')
# 2 - Déterminer les emplacements du document signé et de la copie non signée à l'aide de flux de fichiers:
with system_helper.io.FileStream(MY_DIR + 'Digitally signed.docx', system_helper.io.FileMode.OPEN) as stream_in:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'DigitalSignatureUtil.LoadAndRemove.FromStream.docx', system_helper.io.FileMode.CREATE) as stream_out:
        aw.digitalsignatures.DigitalSignatureUtil.remove_all_signatures(src_stream=stream_in, dst_stream=stream_out)
# Vérifier que nos deux documents de sortie ne contiennent aucune signature numérique.
self.assertEqual(0, aw.digitalsignatures.DigitalSignatureUtil.load_signatures(file_name=ARTIFACTS_DIR + 'DigitalSignatureUtil.LoadAndRemove.FromString.docx').count)
self.assertEqual(0, aw.digitalsignatures.DigitalSignatureUtil.load_signatures(file_name=ARTIFACTS_DIR + 'DigitalSignatureUtil.LoadAndRemove.FromStream.docx').count)
```

## See Also

* module [aspose.words.digitalsignatures](../../)
* class [DigitalSignatureUtil](../)

