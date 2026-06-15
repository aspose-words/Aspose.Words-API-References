---
title: FieldFillIn.prompt_once_on_mail_merge property
linktitle: prompt_once_on_mail_merge property
articleTitle: prompt_once_on_mail_merge property
second_title: Aspose.Words for Python
description: "FieldFillIn.prompt_once_on_mail_merge property. Gets or sets whether the user response should be recieved once per a mail merge operation."
type: docs
weight: 30
url: /python-net/aspose.words.fields/fieldfillin/prompt_once_on_mail_merge/
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
# Insert a FILLIN field. When we manually update this field in Microsoft Word,
# it will prompt us to enter a response. The field will then display the response as text.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_FILL_IN, update_field=True).as_field_fill_in()
field.prompt_text = 'Please enter a response:'
field.default_response = 'A default response.'
# We can also use these fields to ask the user for a unique response for each page
# created during a mail merge done using Microsoft Word.
field.prompt_once_on_mail_merge = True
self.assertEqual(' FILLIN  "Please enter a response:" \\d "A default response." \\o', field.get_field_code())
merge_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_MERGE_FIELD, update_field=True).as_field_merge_field()
merge_field.field_name = 'MergeField'
# If we perform a mail merge programmatically, we can use a custom prompt respondent
# to automatically edit responses for FILLIN fields that the mail merge encounters.
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

