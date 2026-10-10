---
title: "Aspose::Words::DocumentBuilder::InsertFootnote metodo"
linktitle: "InsertFootnote"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder::InsertFootnote metodo. Inserisce una nota a piè di pagina o una nota finale nel documento in C++."
type: docs
weight: 35000
url: /it/cpp/aspose.words/documentbuilder/insertfootnote/
---
## DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType, const System::String\&) method


Inserisce una nota a piè di pagina o una nota finale nel documento.

```cpp
System::SharedPtr<Aspose::Words::Notes::Footnote> Aspose::Words::DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType footnoteType, const System::String &footnoteText)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| footnoteType | Aspose::Words::Notes::FootnoteType | Specifica se inserire una nota a piè di pagina o una nota finale. |
| footnoteText | const System::String\& | Specifica il testo della nota a piè di pagina. |

### ReturnValue

Restituisce un oggetto nota a piè di pagina appena creato.

## Esempi



Mostra come fare riferimento a del testo con una nota a piè di pagina e una nota finale.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci del testo e contrassegnalo con una nota a piè di pagina con la proprietà IsAuto impostata su "true" per impostazione predefinita,
// in modo che il marcatore visualizzato nel testo principale sia numerato automaticamente a "1",
// e la nota a piè di pagina apparirà in fondo alla pagina.
builder->Write(u"This text will be referenced by a footnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote comment regarding referenced text.");

// Inserisci altro testo e contrassegnalo con una nota finale con un marcatore di riferimento personalizzato,
// che verrà usato al posto del numero "2" e imposterà "IsAuto" su false.
builder->Write(u"This text will be referenced by an endnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote comment regarding referenced text.", u"CustomMark");

// Le note a piè di pagina appaiono sempre in fondo al loro testo di riferimento,
// quindi questo interruzione di pagina non influenzerà la nota a piè di pagina.
// D'altra parte, le note finali sono sempre alla fine del documento
// in modo che questa interruzione di pagina spinga la nota finale alla pagina successiva.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFootnote.docx");
```

## Vedi anche

* Class [Footnote](../../../aspose.words.notes/footnote/)
* Enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType, const System::String\&, const System::String\&) method


Inserisce una nota a piè di pagina o una nota finale nel documento.

```cpp
System::SharedPtr<Aspose::Words::Notes::Footnote> Aspose::Words::DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType footnoteType, const System::String &footnoteText, const System::String &referenceMark)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| footnoteType | Aspose::Words::Notes::FootnoteType | Specifica se inserire una nota a piè di pagina o una nota finale. |
| footnoteText | const System::String\& | Specifica il testo della nota a piè di pagina. |
| referenceMark | const System::String\& | Specifica il segno di riferimento personalizzato della nota a piè di pagina. |

### ReturnValue

Restituisce un oggetto nota a piè di pagina appena creato.

## Esempi



Mostra come fare riferimento a del testo con una nota a piè di pagina e una nota finale.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci del testo e contrassegnalo con una nota a piè di pagina con la proprietà IsAuto impostata su "true" per impostazione predefinita,
// in modo che il marcatore visualizzato nel testo principale sia numerato automaticamente a "1",
// e la nota a piè di pagina apparirà in fondo alla pagina.
builder->Write(u"This text will be referenced by a footnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote comment regarding referenced text.");

// Inserisci altro testo e contrassegnalo con una nota finale con un marcatore di riferimento personalizzato,
// che verrà usato al posto del numero "2" e imposterà "IsAuto" su false.
builder->Write(u"This text will be referenced by an endnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote comment regarding referenced text.", u"CustomMark");

// Le note a piè di pagina appaiono sempre in fondo al loro testo di riferimento,
// quindi questo interruzione di pagina non influenzerà la nota a piè di pagina.
// D'altra parte, le note finali sono sempre alla fine del documento
// in modo che questa interruzione di pagina spinga la nota finale alla pagina successiva.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFootnote.docx");
```

## Vedi anche

* Class [Footnote](../../../aspose.words.notes/footnote/)
* Enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
