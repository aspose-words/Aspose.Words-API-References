---
title: FieldFillIn.prompt_once_on_mail_merge property
linktitle: prompt_once_on_mail_merge property
articleTitle: prompt_once_on_mail_merge property
second_title: Aspose.Words for Python
description: "FieldFillIn.prompt_once_on_mail_merge property. Gets or sets whether the user response should be recieved once per a mail merge operation."
type: docs
weight: 30
url: /fr/python-net/aspose.words.fields/fieldfillin/prompt_once_on_mail_merge/
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
# Insérez un champ FILLIN. Lorsque nous mettons à jour manuellement ce champ dans Microsoft Word,
# il nous demandera de saisir une réponse. Le champ affichera alors la réponse sous forme de texte.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_FILL_IN, update_field=True).as_field_fill_in()
field.prompt_text = 'Please enter a response:'
field.default_response = 'A default response.'
# Nous pouvons également utiliser ces champs pour demander à l'utilisateur une réponse unique pour chaque page
# créée lors d'une fusion de courrier effectuée avec Microsoft Word.
field.prompt_once_on_mail_merge = True
self.assertEqual(' FILLIN  "Please enter a response:" \\d "A default response." \\o', field.get_field_code())
merge_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_MERGE_FIELD, update_field=True).as_field_merge_field()
merge_field.field_name = 'MergeField'
# Si nous effectuons une fusion de courrier de manière programmatique, nous pouvons utiliser un répondant d'invite personnalisé
# pour modifier automatiquement les réponses des champs FILLIN rencontrés lors de la fusion de courrier.
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

