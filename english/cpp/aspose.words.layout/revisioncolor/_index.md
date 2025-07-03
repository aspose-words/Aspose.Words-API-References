---
title: Aspose::Words::Layout::RevisionColor enum
linktitle: RevisionColor
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::RevisionColor enum. Allows to specify color of document revisions in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.layout/revisioncolor/
---
## RevisionColor enum


Allows to specify color of document revisions.

```cpp
enum class RevisionColor
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Auto | 0 | Default. |
| Black | 1 | Represents 000000 color. |
| Blue | 2 | Represents 2e97d3 color. |
| BrightGreen | 3 | Represents 84a35b color. |
| ClassicBlue | 4 | Represents 0000ff color. |
| ClassicRed | 5 | Represents ff0000 color. |
| DarkBlue | 6 | Represents 376e96 color. |
| DarkRed | 7 | Represents 881824 color. |
| DarkYellow | 8 | Represents e09a2b color. |
| Gray25 | 9 | Represents a0a3a9 color. |
| Gray50 | 10 | Represents 50565e color. |
| Green | 11 | Represents 2c6234 color. |
| Pink | 12 | Represents ce338f color. |
| Red | 13 | Represents b5082e color. |
| Teal | 14 | Represents 1b9cab color. |
| Turquoise | 15 | Represents 3eafc2 color. |
| Violet | 16 | Represents 633277 color. |
| White | 17 | Represents ffffff color. |
| Yellow | 18 | Represents fad272 color. |
| LightPink | 19 | Represents fce6f4 color. |
| LightBlue | 20 | Represents e1f2fa color. |
| LightYellow | 21 | Represents fef4de color. |
| LightPurple | 22 | Represents eadfef color. |
| LightOrange | 23 | Represents fce3d0 color. |
| LightGreen | 24 | Represents e9f8ce color. |
| Gray | 25 | Represents efeded color. |
| NoHighlight | 26 | No color is used to highlight revision changes. |
| ByAuthor | 27 | Revisions of each author receive their own color for highlighting from a predefined set of hi-contrast colors. |


## Examples



Shows how to alter the appearance of revisions in a rendered output document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a revision, then change the color of all revisions to green.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Remove the bar that appears to the left of every revised line.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## See Also

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
