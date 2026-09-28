---
title: FieldToa class
linktitle: FieldToa class
articleTitle: FieldToa class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldToa class. Implements the TOA field"
type: docs
weight: 1060
url: /fr/python-net/aspose.words.fields/fieldtoa/
---

## FieldToa class

Implements the TOA field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Builds a table of authorities (that is, a list of the references in a legal document, such as references
to cases, statutes, and rules, along with the numbers of the pages on which the references appear) using the
entries specified by TA fields.


**Inheritance:** [FieldToa](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldToa()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmark_name](./bookmark_name/) | Gets or sets the name of the bookmark that marks the portion of the document used to build the table. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [entry_category](./entry_category/) | Gets or sets the integral category for entries included in the table. |
| [entry_separator](./entry_separator/) | Gets or sets the character sequence that is used to separate a table of authorities entry and its page number. |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [page_number_list_separator](./page_number_list_separator/) | Gets or sets the character sequence that is used to separate two page numbers in a page number list. |
| [page_range_separator](./page_range_separator/) | Gets or sets the character sequence that is used to separate the start and end of a page range. |
| [remove_entry_formatting](./remove_entry_formatting/) | Gets or sets whether to remove the formatting of the entry text in the document from the entry in the table of authorities. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [sequence_name](./sequence_name/) | Gets or sets the name of a sequence whose number is included with the page number. |
| [sequence_separator](./sequence_separator/) | Gets or sets the character sequence that is used to separate sequence numbers and page numbers. |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |
| [use_heading](./use_heading/) | Gets or sets whether to include the category heading for the entries in a table of authorities. |
| [use_passim](./use_passim/) | Gets or sets whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited. |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

### Examples

Shows how to build and customize a table of authorities using TOA and TA fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insérez un champ TOA, qui créera une entrée pour chaque champ TA dans le document,
# affichant des citations longues et les numéros de page pour chaque entrée.
field_toa = builder.insert_field(field_type=FieldType.FIELD_TOA, update_field=False).as_field_toa()
# Définissez la catégorie d'entrée pour notre tableau. Ce TOA n'inclura désormais que les champs TA
# qui ont une valeur correspondante dans leur propriété EntryCategory.
field_toa.entry_category = '1'
# De plus, la catégorie Table of Authorities à l'index 1 est "Cases",
# qui apparaîtra comme le titre de notre tableau si nous définissons cette variable sur true.
field_toa.use_heading = True
# Nous pouvons filtrer davantage les champs TA en nommant un signet dans lequel ils devront se trouver à l'intérieur des limites du TOA.
field_toa.bookmark_name = 'MyBookmark'
# Par défaut, un onglet en pointillé sur toute la page apparaît entre la citation du champ TA
# et son numéro de page. Nous pouvons le remplacer par n'importe quel texte que nous mettons dans cette propriété.
# Insérer un caractère de tabulation préservera la tabulation originale.
field_toa.entry_separator = ' \t p.'
# Si nous avons plusieurs entrées TA qui partagent la même citation longue,
# tous leurs numéros de page respectifs apparaîtront sur une même ligne.
# Nous pouvons utiliser cette propriété pour spécifier une chaîne qui séparera leurs numéros de page.
field_toa.page_number_list_separator = ' & p. '
# Nous pouvons définir cela sur true pour que notre tableau affiche le mot "passim"
# si cinq numéros de page ou plus se trouvent sur une même ligne.
field_toa.use_passim = True
# Un champ TA peut faire référence à une plage de pages.
# Nous pouvons spécifier une chaîne ici pour qu'elle apparaisse entre le numéro de page de début et celui de fin pour ces plages.
field_toa.page_range_separator = ' to '
# Le format provenant des champs TA sera repris dans notre tableau.
# Nous pouvons désactiver cela en définissant le drapeau RemoveEntryFormatting.
field_toa.remove_entry_formatting = True
builder.font.color = Color.green
builder.font.name = 'Arial Black'
self.assertEqual(' TOA  \\c 1 \\h \\b MyBookmark \\e " \t p." \\l " & p. " \\p \\g " to " \\f', field_toa.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Ce champ TA n'apparaîtra pas comme une entrée dans le TOA car il est en dehors
# des limites du signet que la propriété BookmarkName du TOA spécifie.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 1')
self.assertEqual(' TA  \\c 1 \\l "Source 1"', field_ta.get_field_code())
# Ce champ TA se trouve à l'intérieur du signet,
# mais la catégorie de l'entrée ne correspond pas à celle du tableau, donc le champ TA ne l'inclura pas.
builder.start_bookmark('MyBookmark')
field_ta = ExField._insert_toa_entry(builder, '2', 'Source 2')
# Cette entrée apparaîtra dans le tableau.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 3')
# Un tableau TOA n'affiche pas les citations courtes,
# mais nous pouvons les utiliser comme abréviation pour faire référence à des noms de sources volumineux que plusieurs champs TA référencent.
field_ta.short_citation = 'S.3'
self.assertEqual(' TA  \\c 1 \\l "Source 3" \\s S.3', field_ta.get_field_code())
# Nous pouvons formater le numéro de page pour le mettre en gras/italique en utilisant les propriétés suivantes.
# Nous verrons toujours ces effets si nous configurons notre tableau pour ignorer le formatage.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 2')
field_ta.is_bold = True
field_ta.is_italic = True
self.assertEqual(' TA  \\c 1 \\l "Source 2" \\b \\i', field_ta.get_field_code())
# Nous pouvons configurer les champs TA pour que leurs entrées TOA fassent référence à une plage de pages couverte par un signet.
# Notez que cette entrée fait référence à la même source que celle ci‑dessus afin de partager une ligne dans notre tableau.
# Cette ligne contiendra le numéro de page de l'entrée ci‑dessus et la plage de pages de cette entrée,
# avec la liste des pages du tableau et les séparateurs de plage de numéros de page entre les numéros de page.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 3')
field_ta.page_range_bookmark_name = 'MyMultiPageBookmark'
builder.start_bookmark('MyMultiPageBookmark')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.end_bookmark('MyMultiPageBookmark')
self.assertEqual(' TA  \\c 1 \\l "Source 3" \\r MyMultiPageBookmark', field_ta.get_field_code())
# Si nous avons activé la fonction "Passim" de notre tableau, le fait d'avoir 5 entrées TA ou plus avec la même source l'activera.
i = 0
while i < 5:
    ExField._insert_toa_entry(builder, '1', 'Source 4')
    i += 1
builder.end_bookmark('MyBookmark')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TOA.TA.docx')
```

Shows how to build and customize a table of authorities using TOA and TA fields (InsertToaEntry).

```python
@staticmethod
def _insert_toa_entry(builder, entry_category, long_citation):
    field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOA_ENTRY, update_field=False).as_field_ta()
    field.entry_category = entry_category
    field.long_citation = long_citation
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    return field
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

