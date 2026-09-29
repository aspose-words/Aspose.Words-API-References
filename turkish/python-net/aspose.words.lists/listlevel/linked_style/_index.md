---
title: ListLevel.linked_style property
linktitle: linked_style property
articleTitle: linked_style property
second_title: Aspose.Words for Python
description: "ListLevel.linked_style property. Gets or sets the paragraph style that is linked to this list level."
type: docs
weight: 60
url: /tr/python-net/aspose.words.lists/listlevel/linked_style/
---

## ListLevel.linked_style property

Gets or sets the paragraph style that is linked to this list level.


```python
@property
def linked_style(self) -> aspose.words.Style:
    ...

@linked_style.setter
def linked_style(self, value: aspose.words.Style):
    ...

```

### Remarks

This property is ``None`` when the list level is not linked to a paragraph style.
This property can be set to ``None``.




### Examples

Shows advances ways of customizing list labels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Bir liste, paragraf gruplarını ön ek sembolleri ve girintilerle düzenlememizi ve süslememizi sağlar.
# Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
# Bir belge oluşturucusunun "ListFormat" özelliğini kullanarak bir listeyi başlatabilir ve sonlandırabiliriz.
# Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf, listenin bir öğesi haline gelecektir.
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
# Seviye 1 etiketleri, "Heading 1" paragraf stiline göre biçimlendirilecek ve bir ön ek alacaktır.
# Bunlar "Appendix A", "Appendix B" gibi görünecek...
doc_list.list_levels[0].number_format = 'Appendix \x00'
doc_list.list_levels[0].number_style = aw.NumberStyle.UPPERCASE_LETTER
doc_list.list_levels[0].linked_style = doc.styles.get_by_name('Heading 1')
# Seviye 2 etiketleri, birinci ve ikinci liste seviyelerinin mevcut sayılarını gösterecek ve başında sıfırlar bulunduracaktır.
# Eğer birinci liste seviyesi 1 ise, bu etiketler "Section (1.01)", "Section (1.02)" gibi görünecektir...
doc_list.list_levels[1].number_format = 'Section (\x00.\x01)'
doc_list.list_levels[1].number_style = aw.NumberStyle.LEADING_ZERO
# Üst seviyenin UppercaseLetter numaralandırmasını kullandığını unutmayın.
# "IsLegal" özelliğini, üst liste seviyeleri için Arap rakamları kullanacak şekilde ayarlayabiliriz.
doc_list.list_levels[1].is_legal = True
doc_list.list_levels[1].restart_after_level = 0
# Seviye 3 etiketleri, bir ön ek ve bir son ek içeren büyük harf Roma rakamları olacak ve her Liste seviyesi 1 öğesinde yeniden başlayacaktır.
# Bu liste etiketleri "-I-", "-II-" gibi görünecek...
doc_list.list_levels[2].number_format = '-\x02-'
doc_list.list_levels[2].number_style = aw.NumberStyle.UPPERCASE_ROMAN
doc_list.list_levels[2].restart_after_level = 1
# Tüm liste seviyelerinin etiketlerini kalın yapın.
for level in doc_list.list_levels:
    level.font.bold = True
# Geçerli paragraf üzerine liste biçimlendirmesini uygulayın.
builder.list_format.list = doc_list
# Üç liste seviyemizin tamamını gösterecek liste öğeleri oluşturun.
n = 0
while n < 2:
    i = 0
    while i < 3:
        builder.list_format.list_level_number = i
        builder.writeln('Level ' + str(i))
        i += 1
    n += 1
builder.list_format.remove_numbers()
doc.save(file_name=ARTIFACTS_DIR + 'Lists.CreateListRestartAfterHigher.docx')
```

### See Also

* module [aspose.words.lists](../../)
* class [ListLevel](../)

