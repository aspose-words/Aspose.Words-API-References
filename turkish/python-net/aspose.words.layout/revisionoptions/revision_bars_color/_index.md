---
title: RevisionOptions.revision_bars_color property
linktitle: revision_bars_color property
articleTitle: revision_bars_color property
second_title: Aspose.Words for Python
description: "RevisionOptions.revision_bars_color property. Allows to specify the color to be used for side bars that identify document lines containing revised information"
type: docs
weight: 150
url: /tr/python-net/aspose.words.layout/revisionoptions/revision_bars_color/
---

## RevisionOptions.revision_bars_color property

Allows to specify the color to be used for side bars that identify document lines containing revised information.
Default value is [RevisionColor.RED](../../revisioncolor/#RED).



```python
@property
def revision_bars_color(self) -> aspose.words.layout.RevisionColor:
    ...

@revision_bars_color.setter
def revision_bars_color(self, value: aspose.words.layout.RevisionColor):
    ...

```

### Remarks

Setting this property  to [RevisionColor.BY_AUTHOR](../../revisioncolor/#BY_AUTHOR) or [RevisionColor.NO_HIGHLIGHT](../../revisioncolor/#NO_HIGHLIGHT) values
will result in hiding revision bars from the layout.


### Examples

Shows how to modify the appearance of revisions.

```python
doc = aw.Document(file_name=MY_DIR + 'Revisions.docx')
# Revizyonların görünümünü kontrol eden RevisionOptions nesnesini alın.
revision_options = doc.layout_options.revision_options
# Ekleme revizyonlarını yeşil ve italik olarak renderlayın.
revision_options.inserted_text_color = aw.layout.RevisionColor.GREEN
revision_options.inserted_text_effect = aw.layout.RevisionTextEffect.ITALIC
# Silme revizyonlarını kırmızı ve kalın olarak renderlayın.
revision_options.deleted_text_color = aw.layout.RevisionColor.RED
revision_options.deleted_text_effect = aw.layout.RevisionTextEffect.BOLD
# Aynı metin bir hareket revizyonunda iki kez görünecek:
# bir kez çıkış noktasında ve bir kez varış noktasında.
# Taşınan-önce revizyonundaki metni çift üstü çizgili sarı olarak renderlayın
# ve taşınan-sonra revizyonunda çift altı çizili mavi olarak.
revision_options.moved_from_text_color = aw.layout.RevisionColor.YELLOW
revision_options.moved_from_text_effect = aw.layout.RevisionTextEffect.DOUBLE_STRIKE_THROUGH
revision_options.moved_to_text_color = aw.layout.RevisionColor.CLASSIC_BLUE
revision_options.moved_to_text_effect = aw.layout.RevisionTextEffect.DOUBLE_UNDERLINE
# Biçim revizyonlarını koyu kırmızı ve kalın olarak renderlayın.
revision_options.revised_properties_color = aw.layout.RevisionColor.DARK_RED
revision_options.revised_properties_effect = aw.layout.RevisionTextEffect.BOLD
# Sayfanın sol tarafına, revizyonlardan etkilenen satırların yanına kalın koyu mavi bir çubuk yerleştirin.
revision_options.revision_bars_color = aw.layout.RevisionColor.DARK_BLUE
revision_options.revision_bars_width = 15
# Revizyon işaretlerini ve orijinal metni gösterin.
revision_options.show_original_revision = True
revision_options.show_revision_marks = True
# Hareket, silme, biçimlendirme revizyonlarını ve yorumları yeşil balonlarda görünür hale getirin
# sayfanın sağ tarafında.
revision_options.show_in_balloons = aw.layout.ShowInBalloons.FORMAT
revision_options.comment_color = aw.layout.RevisionColor.BRIGHT_GREEN
# Bu özellikler yalnızca .pdf veya .jpg gibi formatlar için geçerlidir.
doc.save(file_name=ARTIFACTS_DIR + 'Revision.RevisionOptions.pdf')
```

### See Also

* module [aspose.words.layout](../../)
* class [RevisionOptions](../)

