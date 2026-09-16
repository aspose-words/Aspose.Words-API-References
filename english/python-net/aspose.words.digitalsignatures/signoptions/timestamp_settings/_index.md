---
title: SignOptions.timestamp_settings property
linktitle: timestamp_settings property
articleTitle: timestamp_settings property
second_title: Aspose.Words for Python
description: "SignOptions.timestamp_settings property. Specifies settings for timestamping the digital signature using an RFC 3161 timestamp authority (TSA)"
type: docs
weight: 120
url: /python-net/aspose.words.digitalsignatures/signoptions/timestamp_settings/
---

## SignOptions.timestamp_settings property

Specifies settings for timestamping the digital signature using an RFC 3161 timestamp authority (TSA).
The default value is ``None`` and the digital signature will not be time-stamped.



```python
@property
def timestamp_settings(self) -> aspose.words.digitalsignatures.DigitalSignatureTimestampSettings:
    ...

@timestamp_settings.setter
def timestamp_settings(self, value: aspose.words.digitalsignatures.DigitalSignatureTimestampSettings):
    ...

```

### Remarks

When this property is set to a valid [DigitalSignatureTimestampSettings](../../digitalsignaturetimestampsettings/) object,
and [SignOptions.xml_dsig_level](../xml_dsig_level/) is set to [XmlDsigLevel.X_AD_ES_T](../../xmldsiglevel/#X_AD_ES_T) or higher,
the digital signature will be time-stamped.



### See Also

* module [aspose.words.digitalsignatures](../../)
* class [SignOptions](../)

