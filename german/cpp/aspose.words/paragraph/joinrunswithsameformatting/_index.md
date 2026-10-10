---
title: "Aspose::Words::Paragraph::JoinRunsWithSameFormatting method"
linktitle: "JoinRunsWithSameFormatting"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Paragraph::JoinRunsWithSameFormatting‑Methode. Fügt Läufe mit derselben Formatierung im Absatz in C++ zusammen."
type: docs
weight: 31000
url: /de/cpp/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph::JoinRunsWithSameFormatting() method


Verbindet Runs mit derselben Formatierung im Absatz.

```cpp
int32_t Aspose::Words::Paragraph::JoinRunsWithSameFormatting()
```


### ReturnValue

Anzahl der durchgeführten Zusammenführungen. Wenn **N** benachbarte Runs zusammengeführt werden, zählen sie als **N - 1** Zusammenführungen.

## Beispiele



Zeigt, wie man Absätze vereinfacht, indem man überflüssige Läufe zusammenführt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie vier Textläufe in den Absatz ein.
builder->Write(u"Run 1. ");
builder->Write(u"Run 2. ");
builder->Write(u"Run 3. ");
builder->Write(u"Run 4. ");

// Wenn wir dieses Dokument in Microsoft Word öffnen, sieht der Absatz wie ein nahtloser Textkörper aus.
// Allerdings besteht er aus vier separaten Läufen mit derselben Formatierung. Fragmentierte Absätze wie dieser
// können auftreten, wenn wir in Microsoft Word Teile eines Absatzes mehrfach manuell bearbeiten.
System::SharedPtr<Aspose::Words::Paragraph> para = builder->get_CurrentParagraph();

ASSERT_EQ(4, para->get_Runs()->get_Count());

// Ändern Sie den Stil des letzten Laufs, um ihn von den ersten drei zu unterscheiden.
para->get_Runs()->idx_get(3)->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Emphasis);

// Wir können die Methode \"JoinRunsWithSameFormatting\" ausführen, um den Inhalt des Dokuments zu optimieren
// indem wir ähnliche Läufe zu einem zusammenführen und deren Gesamtzahl reduzieren.
// Diese Methode gibt außerdem die Anzahl der Läufe zurück, die sie zusammengeführt hat.
// Diese beiden Zusammenführungen erfolgten, um die Läufe #1, #2 und #3 zu kombinieren,
// während Lauf #4 ausgelassen wurde, weil er einen inkompatiblen Stil hat.
ASSERT_EQ(2, para->JoinRunsWithSameFormatting());

// Die verbleibende Anzahl von Läufen entspricht der ursprünglichen Anzahl
// abzüglich der Anzahl von Lauf‑Zusammenführungen, die die Methode \"JoinRunsWithSameFormatting\" durchgeführt hat.
ASSERT_EQ(2, para->get_Runs()->get_Count());
ASSERT_EQ(u"Run 1. Run 2. Run 3. ", para->get_Runs()->idx_get(0)->get_Text());
ASSERT_EQ(u"Run 4. ", para->get_Runs()->idx_get(1)->get_Text());
```

## Siehe auch

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::JoinRunsWithSameFormatting(const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\&) method


Verbindet Runs mit derselben Formatierung im Absatz.

```cpp
int32_t Aspose::Words::Paragraph::JoinRunsWithSameFormatting(const System::SharedPtr<Aspose::Words::JoinRunsOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| options | const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\& | Zusätzliche Optionen |

### ReturnValue

Anzahl der durchgeführten Zusammenführungen. Wenn **N** benachbarte Runs zusammengeführt werden, zählen sie als **N - 1** Zusammenführungen.

## Beispiele



Zeigt, wie Runs mit gleicher Formatierung zusammengeführt werden, während redundante und unbedeutende Attribute ignoriert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstellen Sie Runs mit identischer sichtbarer Formatierung, aber einigen internen Unterschieden.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(12);
builder->Write(u"Hello ");
builder->Write(u"world");

// Überprüfen Sie die Runs vor dem Zusammenführen.
ASSERT_EQ(2, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello ", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());
ASSERT_EQ(u"world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(1)->get_Text());

// Konfigurieren Sie Optionen, um redundante und unbedeutende Attribute beim Zusammenführen zu ignorieren.
auto options = System::MakeObject<Aspose::Words::JoinRunsOptions>();
options->set_IgnoreRedundant(true);
// Ignorieren Sie redundante Lauf-Eigenschaften, die das Aussehen nicht beeinflussen.
options->set_IgnoreInsignificant(true);
// Ignorieren Sie unbedeutende Unterschiede wie nur aus Leerzeichen bestehende Läufe.

// Führen Sie Läufe zusammen, die dieselbe sichtbare Formatierung haben, indem Sie die erweiterten Optionen verwenden.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->JoinRunsWithSameFormatting(options);

// Verifizieren Sie, dass die Läufe erfolgreich zusammengeführt wurden.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());

doc->Save(get_ArtifactsDir() + u"Paragraph.JoinRunsWithSameFormattingWithOptions.docx");
```

## Siehe auch

* Class [JoinRunsOptions](../../joinrunsoptions/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
