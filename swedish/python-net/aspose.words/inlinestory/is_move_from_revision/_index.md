---
title: InlineStory.is_move_from_revision property
linktitle: is_move_from_revision property
articleTitle: is_move_from_revision property
second_title: Aspose.Words for Python
description: "InlineStory.is_move_from_revision property. Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled."
type: docs
weight: 50
url: /sv/python-net/aspose.words/inlinestory/is_move_from_revision/
---

## InlineStory.is_move_from_revision property

Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.



```python
@property
def is_move_from_revision(self) -> bool:
    ...

```

### Examples

Shows how to view revision-related properties of InlineStory nodes.

```python
doc = aw.Document(file_name=MY_DIR + 'Revision footnotes.docx')
# När vi redigerar dokumentet medan "Track Changes"-alternativet, som finns via Review -> Tracking,
# är påslaget i Microsoft Word, räknas de ändringar vi gör som revisioner.
# När vi redigerar ett dokument med Aspose.Words kan vi börja spåra revisioner genom att
# anropa dokumentets "StartTrackRevisions"-metod och sluta spåra genom att använda "StopTrackRevisions"-metoden.
# Vi kan antingen acceptera revisioner för att införliva dem i dokumentet
# eller avvisa dem för att ångra och förkasta det föreslagna ändringen.
self.assertTrue(doc.has_revisions)
footnotes = list(map(lambda x: x.as_footnote(), list(doc.get_child_nodes(aw.NodeType.FOOTNOTE, True))))
self.assertEqual(5, len(footnotes))
# Nedan finns fem typer av revisioner som kan flagga en InlineStory-nod.
# 1 -  En "insert"-revision:
# Denna revision uppstår när vi infogar text medan vi spårar ändringar.
self.assertTrue(footnotes[2].is_insert_revision)
# 2 -  En "move from"-revision:
# När vi markerar text i Microsoft Word och sedan drar den till en annan plats i dokumentet
# medan vi spårar ändringar, visas två revisioner.
# "move from"-revisionen är en kopia av texten som ursprungligen fanns innan vi flyttade den.
self.assertTrue(footnotes[4].is_move_from_revision)
# 3 -  En "move to"-revision:
# "move to"-revisionen är den text som vi flyttade till sin nya position i dokumentet.
# "Move from"- och "move to"-revisioner visas i par för varje flyttrevision vi utför.
# Att acceptera en flyttrevision tar bort "move from"-revisionen och dess text,
# och behåller texten från "move to"-revisionen.
# Att avvisa en flyttrevision behåller däremot "move from"-revisionen och tar bort "move to"-revisionen.
self.assertTrue(footnotes[1].is_move_to_revision)
# 4 -  En "delete"-revision:
# Denna revision uppstår när vi tar bort text medan vi spårar ändringar. När vi tar bort text på detta sätt,
# kommer den att finnas kvar i dokumentet som en revision tills vi antingen accepterar revisionen,
# vilket kommer att radera texten permanent, eller avvisa revisionen, vilket kommer att behålla den text vi raderade där den var.
self.assertTrue(footnotes[3].is_delete_revision)
```

### See Also

* module [aspose.words](../../)
* class [InlineStory](../)

