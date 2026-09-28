---
title: FieldFillIn.prompt_text property
linktitle: prompt_text property
articleTitle: prompt_text property
second_title: Aspose.Words for Python
description: "FieldFillIn.prompt_text property. Gets or sets the prompt text (the title of the prompt window)."
type: docs
weight: 40
url: /zh/python-net/aspose.words.fields/fieldfillin/prompt_text/
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
# 插入一个 FILLIN 域。当我们在 Microsoft Word 中手动更新此域时，
# 它会提示我们输入响应。该域随后会以文本形式显示响应。
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_FILL_IN, update_field=True).as_field_fill_in()
field.prompt_text = 'Please enter a response:'
field.default_response = 'A default response.'
# 我们也可以使用这些域来要求用户为每页提供唯一的响应
# 该响应在使用 Microsoft Word 执行邮件合并时创建。
field.prompt_once_on_mail_merge = True
self.assertEqual(' FILLIN  "Please enter a response:" \\d "A default response." \\o', field.get_field_code())
merge_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_MERGE_FIELD, update_field=True).as_field_merge_field()
merge_field.field_name = 'MergeField'
# 如果我们以编程方式执行邮件合并，可以使用自定义提示响应器
# 自动编辑邮件合并遇到的 FILLIN 域的响应。
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

