---
title: "Aspose::Words::Fields::FieldSeq::get_InsertNextNumber Methode"
linktitle: "get_InsertNextNumber"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldSeq::get_InsertNextNumber Methode. Gibt zurück oder legt fest, ob die nächste Sequenznummer für das angegebene Element in C++ eingefügt werden soll."
type: docs
weight: 3000
url: /de/cpp/aspose.words.fields/fieldseq/get_insertnextnumber/
---
## FieldSeq::get_InsertNextNumber method


Liest oder legt fest, ob die nächste Sequenznummer für das angegebene Element eingefügt werden soll.

```cpp
bool Aspose::Words::Fields::FieldSeq::get_InsertNextNumber()
```


## Beispiele



Zeigt das Erstellen von Nummerierungen mit SEQ‑Feldern.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// SEQ-Felder zeigen einen Zähler an, der bei jedem SEQ-Feld inkrementiert wird.
// Diese Felder führen zudem separate Zähler für jede eindeutig benannte Sequenz
// identifiziert durch die "SequenceIdentifier"-Eigenschaft des SEQ-Feldes.
// Fügen Sie ein SEQ‑Feld ein, das den aktuellen Zählwert von "MySequence" anzeigt,
// nachdem die Eigenschaft "ResetNumber" verwendet wurde, um sie auf 100 zu setzen.
builder->Write(u"#");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetNumber(u"100");
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\r 100", fieldSeq->GetFieldCode());
ASSERT_EQ(u"100", fieldSeq->get_Result());

// Zeigen Sie die nächste Nummer in dieser Sequenz mit einem weiteren SEQ‑Feld an.
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->Update();

ASSERT_EQ(u"101", fieldSeq->get_Result());

// Fügen Sie eine Überschrift der Ebene 1 ein.
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"This level 1 heading will reset MySequence to 1");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));

// Fügen Sie ein weiteres SEQ‑Feld aus derselben Sequenz ein und konfigurieren Sie es so, dass die Zählung bei jeder Überschrift mit 1 zurückgesetzt wird.
builder->Write(u"\n#");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetHeadingLevel(u"1");
fieldSeq->Update();

// Die obige Überschrift ist eine Überschrift der Ebene 1, sodass die Zählung für diese Sequenz auf 1 zurückgesetzt wird.
ASSERT_EQ(u" SEQ  MySequence \\s 1", fieldSeq->GetFieldCode());
ASSERT_EQ(u"1", fieldSeq->get_Result());

// Gehen Sie zur nächsten Nummer dieser Sequenz.
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_InsertNextNumber(true);
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\n", fieldSeq->GetFieldCode());
ASSERT_EQ(u"2", fieldSeq->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.ResetNumbering.docx");
```

## Siehe auch

* Class [FieldSeq](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
