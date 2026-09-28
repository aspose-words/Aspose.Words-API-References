---
title: DigitalSignatureUtil.load_signatures method
linktitle: load_signatures method
articleTitle: load_signatures method
second_title: Aspose.Words for Python
description: "aspose.words.digitalsignatures.DigitalSignatureUtil.load_signatures method"
type: docs
weight: 10
url: /de/python-net/aspose.words.digitalsignatures/digitalsignatureutil/load_signatures/
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
# Es gibt zwei Möglichkeiten, die Sammlung digitaler Signaturen eines signierten Dokuments mit der Klasse DigitalSignatureUtil zu laden.
# 1 -  Laden eines Dokuments von einem lokalen Dateisystem anhand des Dateinamens:
digital_signatures = aw.digitalsignatures.DigitalSignatureUtil.load_signatures(file_name=MY_DIR + 'Digitally signed.docx')
# Wenn diese Sammlung nicht leer ist, können wir überprüfen, ob das Dokument digital signiert ist.
self.assertEqual(1, digital_signatures.count)
# 2 -  Laden eines Dokuments aus einem FileStream:
with system_helper.io.FileStream(MY_DIR + 'Digitally signed.docx', system_helper.io.FileMode.OPEN) as stream:
    digital_signatures = aw.digitalsignatures.DigitalSignatureUtil.load_signatures(stream=stream)
    self.assertEqual(1, digital_signatures.count)
```

Shows how to remove digital signatures from a digitally signed document.

```python
# Es gibt zwei Möglichkeiten, die Klasse DigitalSignatureUtil zu verwenden, um digitale Signaturen zu entfernen
# aus einem signierten Dokument, indem man eine unsignierte Kopie davon an einem anderen Ort im lokalen Dateisystem speichert.
# 1 - Bestimmen Sie die Speicherorte sowohl des signierten Dokuments als auch der unsignierten Kopie anhand von Dateinamen-Strings:
aw.digitalsignatures.DigitalSignatureUtil.remove_all_signatures(src_file_name=MY_DIR + 'Digitally signed.docx', dst_file_name=ARTIFACTS_DIR + 'DigitalSignatureUtil.LoadAndRemove.FromString.docx')
# 2 - Bestimmen Sie die Speicherorte sowohl des signierten Dokuments als auch der unsignierten Kopie anhand von FileStreams:
with system_helper.io.FileStream(MY_DIR + 'Digitally signed.docx', system_helper.io.FileMode.OPEN) as stream_in:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'DigitalSignatureUtil.LoadAndRemove.FromStream.docx', system_helper.io.FileMode.CREATE) as stream_out:
        aw.digitalsignatures.DigitalSignatureUtil.remove_all_signatures(src_stream=stream_in, dst_stream=stream_out)
# Verifizieren Sie, dass beide Ausgabedokumente keine digitalen Signaturen enthalten.
self.assertEqual(0, aw.digitalsignatures.DigitalSignatureUtil.load_signatures(file_name=ARTIFACTS_DIR + 'DigitalSignatureUtil.LoadAndRemove.FromString.docx').count)
self.assertEqual(0, aw.digitalsignatures.DigitalSignatureUtil.load_signatures(file_name=ARTIFACTS_DIR + 'DigitalSignatureUtil.LoadAndRemove.FromStream.docx').count)
```

## See Also

* module [aspose.words.digitalsignatures](../../)
* class [DigitalSignatureUtil](../)

