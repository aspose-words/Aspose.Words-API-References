---
title: "Aspose::Words::JoinRunsOptions Klasse"
linktitle: "JoinRunsOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::JoinRunsOptions Klasse. Stellt Konfigurationsflags für die JoinRuns-Operation in C++ bereit."
type: docs
weight: 38500
url: /de/cpp/aspose.words/joinrunsoptions/
---
## JoinRunsOptions class


Stellt Konfigurationsflags für die Join‑Runs‑Operation bereit.

```cpp
class JoinRunsOptions : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_IgnoreInsignificant](./get_ignoreinsignificant/)() const | Wahr zeigt an, dass die unbedeutenden Attribute aller Runs beim Zusammenführen von Runs mit gleicher Formatierung ignoriert werden. |
| [get_IgnoreRedundant](./get_ignoreredundant/)() const | Wahr zeigt an, dass die redundanten Attribute aller Runs beim Zusammenführen von Runs mit gleicher Formatierung ignoriert werden. |
| [get_IgnoreSpacing](./get_ignorespacing/)() const | Wahr zeigt an, dass die Abstandsattribute aller Runs beim Zusammenführen von Runs mit gleicher Formatierung ignoriert werden. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [JoinRunsOptions](./joinrunsoptions/)() |  |
| [set_IgnoreInsignificant](./set_ignoreinsignificant/)(bool) | Wahr zeigt an, dass die unbedeutenden Attribute aller Runs beim Zusammenführen von Runs mit gleicher Formatierung ignoriert werden. |
| [set_IgnoreRedundant](./set_ignoreredundant/)(bool) | Wahr zeigt an, dass die redundanten Attribute aller Runs beim Zusammenführen von Runs mit gleicher Formatierung ignoriert werden. |
| [set_IgnoreSpacing](./set_ignorespacing/)(bool) | Wahr zeigt an, dass die Abstandsattribute aller Runs beim Zusammenführen von Runs mit gleicher Formatierung ignoriert werden. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
