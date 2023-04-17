---
title: Aspose::Words::DocumentBuilder::InsertFootnote method
linktitle: InsertFootnote
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::InsertFootnote method. Inserts a footnote or endnote into the document in C++.'
type: docs
weight: 35000
url: /cpp/aspose.words/documentbuilder/insertfootnote/
---
## DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType, const System::String\&) method


Inserts a footnote or endnote into the document.

```cpp
System::SharedPtr<Aspose::Words::Notes::Footnote> Aspose::Words::DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType footnoteType, const System::String &footnoteText)
```


| Parameter | Type | Description |
| --- | --- | --- |
| footnoteType | Aspose::Words::Notes::FootnoteType | Specifies whether to insert a footnote or an endnote. |
| footnoteText | const System::String\& | Specifies the text of the footnote. |

### ReturnValue

Returns a footnote object that was just created.

## Examples



Shows how to reference text with a footnote and an endnote. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert some text and mark it with a footnote with the IsAuto property set to "true" by default,
// so the marker seen in the body text will be auto-numbered at "1",
// and the footnote will appear at the bottom of the page.
builder->Write(u"This text will be referenced by a footnote.");
builder->InsertFootnote(FootnoteType::Footnote, u"Footnote comment regarding referenced text.");

// Insert more text and mark it with an endnote with a custom reference mark,
// which will be used in place of the number "2" and set "IsAuto" to false.
builder->Write(u"This text will be referenced by an endnote.");
builder->InsertFootnote(FootnoteType::Endnote, u"Endnote comment regarding referenced text.", u"CustomMark");

// Footnotes always appear at the bottom of their referenced text,
// so this page break will not affect the footnote.
// On the other hand, endnotes are always at the end of the document
// so that this page break will push the endnote down to the next page.
builder->InsertBreak(BreakType::PageBreak);

doc->Save(ArtifactsDir + u"DocumentBuilder.InsertFootnote.docx");
```

## See Also

* Class [Footnote](../../../aspose.words.notes/footnote/)
* Enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType, const System::String\&, const System::String\&) method


Inserts a footnote or endnote into the document.

```cpp
System::SharedPtr<Aspose::Words::Notes::Footnote> Aspose::Words::DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType footnoteType, const System::String &footnoteText, const System::String &referenceMark)
```


| Parameter | Type | Description |
| --- | --- | --- |
| footnoteType | Aspose::Words::Notes::FootnoteType | Specifies whether to insert a footnote or an endnote. |
| footnoteText | const System::String\& | Specifies the text of the footnote. |
| referenceMark | const System::String\& | Specifies the custom reference mark of the footnote. |

### ReturnValue

Returns a footnote object that was just created.

## Examples



Shows how to reference text with a footnote and an endnote. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert some text and mark it with a footnote with the IsAuto property set to "true" by default,
// so the marker seen in the body text will be auto-numbered at "1",
// and the footnote will appear at the bottom of the page.
builder->Write(u"This text will be referenced by a footnote.");
builder->InsertFootnote(FootnoteType::Footnote, u"Footnote comment regarding referenced text.");

// Insert more text and mark it with an endnote with a custom reference mark,
// which will be used in place of the number "2" and set "IsAuto" to false.
builder->Write(u"This text will be referenced by an endnote.");
builder->InsertFootnote(FootnoteType::Endnote, u"Endnote comment regarding referenced text.", u"CustomMark");

// Footnotes always appear at the bottom of their referenced text,
// so this page break will not affect the footnote.
// On the other hand, endnotes are always at the end of the document
// so that this page break will push the endnote down to the next page.
builder->InsertBreak(BreakType::PageBreak);

doc->Save(ArtifactsDir + u"DocumentBuilder.InsertFootnote.docx");
```

## See Also

* Class [Footnote](../../../aspose.words.notes/footnote/)
* Enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
