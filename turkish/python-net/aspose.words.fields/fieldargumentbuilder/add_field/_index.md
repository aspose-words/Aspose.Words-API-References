---
title: FieldArgumentBuilder.add_field method
linktitle: add_field method
articleTitle: add_field method
second_title: Aspose.Words for Python
description: "FieldArgumentBuilder.add_field method. Adds a field represented by a [FieldBuilder](../../fieldbuilder/) to the argument."
type: docs
weight: 20
url: /tr/python-net/aspose.words.fields/fieldargumentbuilder/add_field/
---

## add_field(field_builder) {#fieldbuilder}

Adds a field represented by a [FieldBuilder](../../fieldbuilder/) to the argument.



```python
def add_field(self, field_builder: aspose.words.fields.FieldBuilder):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| field_builder | [FieldBuilder](../../fieldbuilder/) |  |

### Examples

Shows how to construct fields using a field builder, and then insert them into the document.

```python
from api_example_base import ApiExampleBase, ARTIFACTS_DIR
import aspose.words as aw
from aspose.words.fields import FieldType, FieldBuilder, FieldArgumentBuilder
doc = aw.Document()
# Aşağıda bir alan oluşturucu kullanılarak yapılan üç alan oluşturma örneği bulunmaktadır.
# 1 -  Tek alan:
# Bir alan oluşturucu kullanarak ƒ (Florin) sembolünü gösteren bir SYMBOL alanı ekleyin.
builder = FieldBuilder(FieldType.FIELD_SYMBOL)
builder.add_argument(argument=402)
builder.add_switch(switch_name='\\f', switch_argument='Arial')
builder.add_switch(switch_name='\\s', switch_argument=25)
builder.add_switch(switch_name='\\u')
field = builder.build_and_insert(ref_node=doc.first_section.body.first_paragraph)
self.assertEqual(' SYMBOL 402 \\f Arial \\s 25 \\u ', field.get_field_code())
# 2 -  İç içe alan:
# Bir alan oluşturucu kullanarak başka bir alan oluşturucu tarafından iç alan olarak kullanılan bir formül alanı oluşturun.
inner_formula_builder = FieldBuilder(FieldType.FIELD_FORMULA)
inner_formula_builder.add_argument(argument=100)
inner_formula_builder.add_argument(argument='+')
inner_formula_builder.add_argument(argument=74)
# Başka bir SYMBOL alanı için başka bir oluşturucu oluşturun ve formül alanını ekleyin
# yukarıda oluşturduğumuz formül alanını SYMBOL alanının argümanı olarak ekleyin.
builder = FieldBuilder(FieldType.FIELD_SYMBOL)
builder.add_argument(argument=inner_formula_builder)
field = builder.build_and_insert(ref_node=doc.first_section.body.append_paragraph(''))
# Harici SYMBOL alanı, formül alanı sonucunu, 174, argümanı olarak kullanacak,
# bu da alanın ® (Kayıtlı İşaret) sembolünü göstermesini sağlayacak, çünkü karakter numarası 174.
self.assertEqual(' SYMBOL \x13 = 100 + 74 \x14\x15 ', field.get_field_code())
# 3 -  Birden çok iç içe alan ve argümanlar:
# Şimdi, iki özel dize değerinden birini gösteren bir IF alanı oluşturmak için bir oluşturucu kullanacağız,
# ifadesinin doğru/yanlış değerine bağlı olarak. Doğru/yanlış bir değer elde etmek için
# hangi dizeyi IF alanının göstereceğini belirleyen, IF alanı iki sayısal ifadeyi eşitlik için test edecek.
# İki ifadeyi formül alanları şeklinde sağlayacağız ve bu alanları IF alanının içine iç içe yerleştireceğiz.
left_expression = FieldBuilder(FieldType.FIELD_FORMULA)
left_expression.add_argument(argument=2)
left_expression.add_argument(argument='+')
left_expression.add_argument(argument=3)
right_expression = FieldBuilder(FieldType.FIELD_FORMULA)
right_expression.add_argument(argument=2.5)
right_expression.add_argument(argument='*')
right_expression.add_argument(argument=5.2)
# Sonra, IF alanı için doğru/yanlış çıktı dizeleri olarak hizmet edecek iki alan argümanı oluşturacağız.
# Bu argümanlar sayısal ifadelerimizin çıktı değerlerini yeniden kullanacak.
true_output = FieldArgumentBuilder()
true_output.add_text('True, both expressions amount to ')
true_output.add_field(left_expression)
false_output = FieldArgumentBuilder()
false_output.add_node(aw.Run(doc=doc, text='False, '))
false_output.add_field(left_expression)
false_output.add_node(aw.Run(doc=doc, text=' does not equal '))
false_output.add_field(right_expression)
# Son olarak, IF alanı için bir oluşturucu daha oluşturacağız ve tüm ifadeleri birleştireceğiz.
builder = FieldBuilder(FieldType.FIELD_IF)
builder.add_argument(argument=left_expression)
builder.add_argument(argument='=')
builder.add_argument(argument=right_expression)
builder.add_argument(argument=true_output)
builder.add_argument(argument=false_output)
field = builder.build_and_insert(ref_node=doc.first_section.body.append_paragraph(''))
self.assertEqual(' IF \x13 = 2 + 3 \x14\x15 = \x13 = 2.5 * 5.2 \x14\x15 ' + '"True, both expressions amount to \x13 = 2 + 3 \x14\x15" ' + '"False, \x13 = 2 + 3 \x14\x15 does not equal \x13 = 2.5 * 5.2 \x14\x15" ', field.get_field_code())
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.SYMBOL.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldArgumentBuilder](../)

