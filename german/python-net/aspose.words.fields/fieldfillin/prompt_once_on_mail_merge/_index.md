---
title: FieldFillIn.prompt_once_on_mail_merge property
linktitle: prompt_once_on_mail_merge property
articleTitle: prompt_once_on_mail_merge property
second_title: Aspose.Words for Python
description: "FieldFillIn.prompt_once_on_mail_merge property. Gets or sets whether the user response should be recieved once per a mail merge operation."
type: docs
weight: 30
url: /de/python-net/aspose.words.fields/fieldfillin/prompt_once_on_mail_merge/
---

## FieldFillIn.prompt_once_on_mail_merge property

Gets or sets whether the user response should be recieved once per a mail merge operation.


```python
@property
def prompt_once_on_mail_merge(self) -> bool:
    ...

@prompt_once_on_mail_merge.setter
def prompt_once_on_mail_merge(self, value: bool):
    ...

```

### Examples

Shows how to use the FILLIN field to prompt the user for a response.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Fügen Sie ein FILLIN-Feld ein. Wenn wir dieses Feld in Microsoft Word manuell aktualisieren,
# wird es uns auffordern, eine Antwort einzugeben. Das Feld wird dann die Antwort als Text anzeigen.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_FILL_IN, update_field=True).as_field_fill_in()
field.prompt_text = 'Please enter a response:'
field.default_response = 'A default response.'
# Wir können diese Felder auch verwenden, um den Benutzer nach einer eindeutigen Antwort für jede Seite zu fragen
# erstellt während eines Seriendrucks, der mit Microsoft Word durchgeführt wird.
field.prompt_once_on_mail_merge = True
self.assertEqual(' FILLIN  "Please enter a response:" \\d "A default response." \\o', field.get_field_code())
merge_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_MERGE_FIELD, update_field=True).as_field_merge_field()
merge_field.field_name = 'MergeField'
# Wenn wir einen Seriendruck programmgesteuert ausführen, können wir einen benutzerdefinierten Prompt-Responder verwenden
# um automatisch Antworten für FILLIN-Felder zu bearbeiten, die der Seriendruck findet.
doc.field_options.user_prompt_respondent = self.PromptRespondent()
doc.mail_merge.execute(field_names=['MergeField'], values=[''])
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.FILLIN.docx')
```

Shows how to use the FILLIN field to prompt the user for a response (PromptRespondent).

```python
class PromptRespondent(aw.fields.IFieldUserPromptRespondent):

    def respond(self, prompt_text, default_response):
        return 'Response modified by PromptRespondent. ' + default_response
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldFillIn](../)

