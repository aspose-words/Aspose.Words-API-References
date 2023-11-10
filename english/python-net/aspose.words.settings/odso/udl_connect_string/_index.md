---
title: Odso.udl_connect_string property
linktitle: udl_connect_string property
articleTitle: udl_connect_string property
second_title: Aspose.Words for Python
description: "Odso.udl_connect_string property. Specifies the Universal Data Link (UDL) connection string used to connect to an external data source"
type: docs
weight: 90
url: /python-net/aspose.words.settings/odso/udl_connect_string/
---

## Odso.udl_connect_string property

Specifies the Universal Data Link (UDL) connection string used to connect to an external data source.
The default value is an empty string.


```python
@property
def udl_connect_string(self) -> str:
    ...

@udl_connect_string.setter
def udl_connect_string(self, value: str):
    ...

```

### Examples

Shows how to execute a mail merge while connecting to an external data source.

```python
doc = aw.Document(MY_DIR + "Odso data.docx")
settings = doc.mail_merge_settings

print(f"Connection string:\n\t{settings.connect_string}")
print(f"Mail merge docs as attachment:\n\t{settings.mail_as_attachment}")
print(f"Mail merge doc e-mail subject:\n\t{settings.mail_subject}")
print(f"Column that contains e-mail addresses:\n\t{settings.address_field_name}")
print(f"Active record:\n\t{settings.active_record}")

odso = settings.odso

print(f"File will connect to data source located in:\n\t\"{odso.data_source}\"")
print(f"Source type:\n\t{odso.data_source_type}")
print(f"UDL connection string:\n\t{odso.udl_connect_string}")
print(f"Table:\n\t{odso.table_name}")
print(f"Query:\n\t{doc.mail_merge_settings.query}")

# We can reset these settings by clearing them. Once we do that and save the document,
# Microsoft Word will no longer execute a mail merge when we use it to load the document.
settings.clear()

doc.save(ARTIFACTS_DIR + "MailMerge.odso_email.docx")
```

### See Also

* module [aspose.words.settings](../../)
* class [Odso](../)

