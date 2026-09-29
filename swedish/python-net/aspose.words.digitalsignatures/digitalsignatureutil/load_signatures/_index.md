---
title: DigitalSignatureUtil.load_signatures method
linktitle: load_signatures method
articleTitle: load_signatures method
second_title: Aspose.Words for Python
description: "aspose.words.digitalsignatures.DigitalSignatureUtil.load_signatures method"
type: docs
weight: 10
url: /sv/python-net/aspose.words.digitalsignatures/digitalsignatureutil/load_signatures/
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
# Det finns två sätt att ladda en signerad dokuments samling av digitala signaturer med hjälp av klassen DigitalSignatureUtil.
# 1 -  Läs in ett dokument från ett lokalt filsystem med filnamn:
digital_signatures = aw.digitalsignatures.DigitalSignatureUtil.load_signatures(file_name=MY_DIR + 'Digitally signed.docx')
# Om den här samlingen inte är tom kan vi verifiera att dokumentet är digitalt signerat.
self.assertEqual(1, digital_signatures.count)
# 2 -  Läs in ett dokument från en FileStream:
with system_helper.io.FileStream(MY_DIR + 'Digitally signed.docx', system_helper.io.FileMode.OPEN) as stream:
    digital_signatures = aw.digitalsignatures.DigitalSignatureUtil.load_signatures(stream=stream)
    self.assertEqual(1, digital_signatures.count)
```

Shows how to remove digital signatures from a digitally signed document.

```python
# Det finns två sätt att använda klassen DigitalSignatureUtil för att ta bort digitala signaturer
# från ett signerat dokument genom att spara en osignerad kopia av det någon annanstans i det lokala filsystemet.
# 1 - Bestäm platserna för både det signerade dokumentet och den osignerade kopian med filnamnsträngar:
aw.digitalsignatures.DigitalSignatureUtil.remove_all_signatures(src_file_name=MY_DIR + 'Digitally signed.docx', dst_file_name=ARTIFACTS_DIR + 'DigitalSignatureUtil.LoadAndRemove.FromString.docx')
# 2 - Bestäm platserna för både det signerade dokumentet och den osignerade kopian med filströmmar:
with system_helper.io.FileStream(MY_DIR + 'Digitally signed.docx', system_helper.io.FileMode.OPEN) as stream_in:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'DigitalSignatureUtil.LoadAndRemove.FromStream.docx', system_helper.io.FileMode.CREATE) as stream_out:
        aw.digitalsignatures.DigitalSignatureUtil.remove_all_signatures(src_stream=stream_in, dst_stream=stream_out)
# Verifiera att båda våra utdata-dokument inte har några digitala signaturer.
self.assertEqual(0, aw.digitalsignatures.DigitalSignatureUtil.load_signatures(file_name=ARTIFACTS_DIR + 'DigitalSignatureUtil.LoadAndRemove.FromString.docx').count)
self.assertEqual(0, aw.digitalsignatures.DigitalSignatureUtil.load_signatures(file_name=ARTIFACTS_DIR + 'DigitalSignatureUtil.LoadAndRemove.FromStream.docx').count)
```

## See Also

* module [aspose.words.digitalsignatures](../../)
* class [DigitalSignatureUtil](../)

