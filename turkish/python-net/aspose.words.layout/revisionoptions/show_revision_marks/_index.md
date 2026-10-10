---
title: RevisionOptions.show_revision_marks property
linktitle: show_revision_marks property
articleTitle: show_revision_marks property
second_title: Aspose.Words for Python
description: "RevisionOptions.show_revision_marks property. Allow to specify whether revision text should be marked with special formatting markup"
type: docs
weight: 210
url: /tr/python-net/aspose.words.layout/revisionoptions/show_revision_marks/
---

## RevisionOptions.show_revision_marks property

Allow to specify whether revision text should be marked with special formatting markup.
Default value is ``True``.



```python
@property
def show_revision_marks(self) -> bool:
    ...

@show_revision_marks.setter
def show_revision_marks(self, value: bool):
    ...

```

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

