---
title: PageSetup.different_first_page_header_footer property
linktitle: different_first_page_header_footer property
articleTitle: different_first_page_header_footer property
second_title: Aspose.Words for Python
description: "PageSetup.different_first_page_header_footer property. True if a different header or footer is used on the first page."
type: docs
weight: 110
url: /fr/python-net/aspose.words/pagesetup/different_first_page_header_footer/
---

## PageSetup.different_first_page_header_footer property

True if a different header or footer is used on the first page.


```python
@property
def different_first_page_header_footer(self) -> bool:
    ...

@different_first_page_header_footer.setter
def different_first_page_header_footer(self, value: bool):
    ...

```

### Examples

Shows how to create headers and footers in a document using DocumentBuilder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Spécifiez que nous voulons des en-têtes et pieds de page différents pour les premières, paires et impaires pages.
builder.page_setup.different_first_page_header_footer = True
builder.page_setup.odd_and_even_pages_header_footer = True
# Créez les en-têtes, puis ajoutez trois pages au document pour afficher chaque type d'en-tête.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_FIRST)
builder.write('Header for the first page')
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_EVEN)
builder.write('Header for even pages')
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write('Header for all other pages')
builder.move_to_section(0)
builder.writeln('Page1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page3')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.HeadersAndFooters.docx')
```

Shows how to track the order in which a text replacement operation traverses nodes.

```python
doc = aw.Document(file_name=MY_DIR + 'Header and footer types.docx')
first_page_section = doc.first_section
logger = self.ReplaceLog()
options = aw.replacing.FindReplaceOptions(replacing_callback=logger)
# Utiliser un en-tête/pied de page différent pour la première page affectera l'ordre de recherche.
first_page_section.page_setup.different_first_page_header_footer = different_first_page_header_footer
doc.range.replace_regex(pattern='(header|footer)', replacement='', options=options)
if different_first_page_header_footer:
    self.assertEqual('First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n', logger.text.replace('\r', ''))
else:
    self.assertEqual('Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n', logger.text.replace('\r', ''))
```

Shows how to track the order in which a text replacement operation traverses nodes (ReplaceLog).

```python
class ReplaceLog(aw.replacing.IReplacingCallback):

    @property
    def text(self):
        return str.join('', self.m_text_builder)

    def __init__(self):
        self.m_text_builder = []

    def replacing(self, args):
        self.m_text_builder.append(args.match_node.get_text() + '\n')
        return aw.replacing.ReplaceAction.SKIP
```

Shows how to enable or disable primary headers/footers.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Ci-dessous se trouvent deux types d'en-têtes/pieds de page.
# 1 -  L'en-tête/pied de page "First", qui apparaît sur la première page de la section.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_FIRST)
builder.writeln('First page header.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_FIRST)
builder.writeln('First page footer.')
# 2 -  L'en-tête/pied de page "Primary", qui apparaît sur chaque page de la section.
# Nous pouvons remplacer l'en-tête/pied de page principal par un en-tête/pied de page de première page et un en-tête/pied de page pair.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.writeln('Primary header.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.writeln('Primary footer.')
builder.move_to_section(0)
builder.writeln('Page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 3.')
# Chaque section possède un objet "PageSetup" qui spécifie les propriétés liées à l'apparence de la page
# telles que l'orientation, la taille et les bordures.
# Définissez la propriété "DifferentFirstPageHeaderFooter" sur "true" pour appliquer le premier en-tête/pied de page à la première page.
# Définissez la propriété "DifferentFirstPageHeaderFooter" sur "false"
# pour que la première page affiche l'en-tête/pied de page principal.
builder.page_setup.different_first_page_header_footer = different_first_page_header_footer
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.DifferentFirstPageHeaderFooter.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

