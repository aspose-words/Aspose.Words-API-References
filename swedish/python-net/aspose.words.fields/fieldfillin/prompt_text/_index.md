---
title: FieldFillIn.prompt_text property
linktitle: prompt_text property
articleTitle: prompt_text property
second_title: Aspose.Words for Python
description: "FieldFillIn.prompt_text property. Gets or sets the prompt text (the title of the prompt window)."
type: docs
weight: 40
url: /sv/python-net/aspose.words.fields/fieldfillin/prompt_text/
---

## FieldFillIn.prompt_text property

Gets or sets the prompt text (the title of the prompt window).


```python
@property
def prompt_text(self) -> str:
    ...

@prompt_text.setter
def prompt_text(self, value: str):
    ...

```

### Examples

Shows how to use the FILLIN field to prompt the user for a response.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Infoga ett FILLIN-fält. När vi manuellt uppdaterar detta fält i Microsoft Word,
# kommer det att be oss ange ett svar. Fältet kommer sedan att visa svaret som text.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_FILL_IN, update_field=True).as_field_fill_in()
field.prompt_text = 'Please enter a response:'
field.default_response = 'A default response.'
# Vi kan också använda dessa fält för att be användaren om ett unikt svar för varje sida
# skapade under en kopplad utskick som görs med Microsoft Word.
field.prompt_once_on_mail_merge = True
self.assertEqual(' FILLIN  "Please enter a response:" \\d "A default response." \\o', field.get_field_code())
merge_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_MERGE_FIELD, update_field=True).as_field_merge_field()
merge_field.field_name = 'MergeField'
# Om vi utför ett kopplat utskick programatiskt, kan vi använda en anpassad prompt‑respondent
# för att automatiskt redigera svar för FILLIN-fält som kopplade utskick stöter på.
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

