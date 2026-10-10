---
title: PdfDigitalSignatureTimestampSettings.user_name property
linktitle: user_name property
articleTitle: user_name property
second_title: Aspose.Words for Python
description: "PdfDigitalSignatureTimestampSettings.user_name property. Timestamp server user name."
type: docs
weight: 50
url: /fr/python-net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/user_name/
---

## PdfDigitalSignatureTimestampSettings.user_name property

Timestamp server user name.


```python
@property
def user_name(self) -> str:
    ...

@user_name.setter
def user_name(self, value: str):
    ...

```

### Remarks

The default value is ``None``.



### Examples

Shows how to sign a saved PDF document digitally and timestamp it.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Signed PDF contents.')
# Créez un objet "PdfSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
# pour modifier la façon dont cette méthode convertit le document en .PDF.
options = aw.saving.PdfSaveOptions()
# Créez une signature numérique et assignez-la à notre objet SaveOptions pour signer le document lorsque nous l'enregistrons au format PDF.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
options.digital_signature_details = aw.saving.PdfDigitalSignatureDetails(certificate_holder, 'Test Signing', 'Aspose Office', datetime.datetime.now())
# Créez un horodatage vérifié par une autorité d'horodatage.
options.digital_signature_details.timestamp_settings = aw.saving.PdfDigitalSignatureTimestampSettings(server_url='https://freetsa.org/tsr', user_name='JohnDoe', password='MyPassword')
# La durée de vie par défaut de l'horodatage est de 100 secondes.
# Nous pouvons définir notre période d'expiration via le constructeur.
options.digital_signature_details.timestamp_settings = aw.saving.PdfDigitalSignatureTimestampSettings(server_url='https://freetsa.org/tsr', user_name='JohnDoe', password='MyPassword', timeout=datetime.timedelta(minutes=30))
self.assertEqual(1800.0, options.digital_signature_details.timestamp_settings.timeout.total_seconds)
self.assertEqual('https://freetsa.org/tsr', options.digital_signature_details.timestamp_settings.server_url)
self.assertEqual('JohnDoe', options.digital_signature_details.timestamp_settings.user_name)
self.assertEqual('MyPassword', options.digital_signature_details.timestamp_settings.password)
# La méthode "Save" appliquera notre signature au document de sortie à ce moment-ci.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfDigitalSignatureTimestampSettings](../)

